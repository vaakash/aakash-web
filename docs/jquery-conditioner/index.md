## Setting Options in Conditioner

Options can be set in two different ways in jQuery conditioner.

- Inline options ( supports only one condition )
- External options ( supports multiple conditions )

[Demo page](/demos/jquery-conditioner/)

## Inline options

Inline options ( `data-condr-*` attributes ) has to be set on the element which has to be shown when an input element has a specific value. jQuery Conditioner has to be enabled on this element later. All the inline options mentioned below are compulsory

    <select id="fruits">
        <option value="apple">Apple</option>
        <option value="banana">Banana</option>
        <option value="mango">Mango</option>
    </select>

    <!-- Plugin options given inline -->
    <div class="banana-section"
    data-condr-input="#fruits"
    data-condr-value="banana"
    data-condr-action="simple?show:hide"
    data-condr-events="click">
        Here are the Banana options ..
    </div>

    <script>$('.banana-section').conditioner();</script>

`data-condr-input`

The input element to check for a value. Below are the possible ways an input element can be selected.

Absolute selector examples ( all jQuery like selectors ):

- `#apple`
- `.strawberry`
- `[name='grapes']`

Example:

    <input type="text" id="mango" />
    <div class="orange" data-condr-input="#mango">My content</div>

Relative selector examples: `(jQuery_method::method_parameters)`

- `(siblings::.wrap1)(find::input[type='text'])`
- `(parent::)(next::)`

Example:

    <div class="row1">
        <input type="text" class="kiwifruit" />
    </div>
    <div class="row2" data-condr-input="(prev::)(find::.kiwifruit)" >My content</div>

`data-condr-value`

This attribute holds the value against which the input element's value has to be checked. It can be a simple value or a regex pattern based on the `data-condr-action` mentioned below

`data-condr-action`

This attribute indicates how the value of the selected input element has to be evaluated and what to do if the input element has that value.

Syntax:

`{type_of_evaluation}?jquery_method_on_value_match:jquery_method_on_no_value_match`

- `type_of_evaluation` - Possible values are,
    - `simple` - Equal match with input's value.
    - `pattern` - Pattern match with input's value. Pattern as to be mentioned in `data-condr-value`
- `jquery_method_on_value_match` - jQuery method to call when value matches. Example: show, hide, slideUp, slideDown, fadeIn, fadeOut
- `jquery_method_on_no_value_match` - jQuery method to call when value does not match. Example: show, hide, slideUp, slideDown, fadeIn, fadeOut

Examples:

    <!-- Ex 1: Simple match, when value of #apple is "tasty", .mango is displayed and hidden otherwise -->
    <input type="text" id="apple" />
    <div data-condr-input="#apple" data-condr-action="simple?show:hide" data-condr-value="tasty" class="mango">My content</div>

    <!-- Ex 2: Pattern match, when value of #apple is an email ID, .mango is displayed and hidden otherwise -->
    <input type="text" id="apple" />
    <div data-condr-input="#apple" data-condr-action="pattern?fadeIn:slideUp" data-condr-value="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,3}$" class="mango">My content</div>

`data-condr-events`

This attribute holds a list of events separated by spaces upon which the condition has to be checked.

Example values:

- `change`
- `click focus`
- `keyup`

## External options

The advantage of external options compared to inline options is multiple conditions can be given ( This feature of external options is just for fun. We can achieve the same thing through simple conditions in if/else conditions. Whereas the inline options feature is a huge time saver.

#### Example:

    <ul>
        <li><input type="text" class="tb3" placeholder="type hey" /></li>
        <li><label><input type="radio" name="agreecheck" value="disagree" /> I Disagree</label> <label><input type="radio" value="agree" name="agreecheck" />I Agree</label>  </li>
        <li><label><input type="checkbox" class="cb2"/> I once again agree to the terms</label></li>
    </ul>
    <div class="multiple1">Thanks.. you can finally <button>Submit</button></div>

    $(document).ready(function(){
        $('.multiple1').conditioner({
            conditions: [
                {
                    input: '.tb3',
                    type: 'simple',
                    value: 'hey'
                },
                {
                    input: '[name=agreecheck]',
                    type: 'simple',
                    value: 'agree'
                },
                {
                    input: '.cb2'
                },
            ],
            events: 'click keyup',
            onTrue: function(){  $(this).fadeIn( 'slow' );  },
            onFalse: function(){  $(this).slideUp( 'slow' );  }
        });
    });