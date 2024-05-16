# JQuery
   $(document).ready(function() {
    });
        #without your document ready function, your code may run before your HTML is rendered, which would cause bugs.
    # All JQuery functions start with a $, usually referred to as a dollar sign operator, or as bling.
       jQuery often selects an HTML element with a selector, then does something to that element.

        For example, let's make all of your button elements bounce. Just add this code inside your document ready function:

        $("button").addClass("animated bounce"); 
    # You just used jQuery's .addClass() function, which allows you to add classes to elements.
        First, let's target your div elements with the class well by using the $(".well") selector.

        Note that, just like with CSS declarations, you type a . before the class's name.

        Then use jQuery's .addClass() function to add the classes animated and shake.
    You can also target elements by their id attributes.

First target your button element with the id target3 by using the $("#target3") selector.

    Note that, just like with CSS declarations, you type a # before the id's name.

    Then use jQuery's .addClass() function to add the classes animated and fadeOut.

    Here's how you'd make the button element with the id target6 fade out:
        $("#target6").addClass("animated fadeOut");

 jQuery has a function called .css() that allows you to change the CSS of an element.

    Here's how we would change its color to blue:

    $("#target1").css("color", "blue");
    This is slightly different from a normal CSS declaration, because the CSS property and its value are in quotes, and separated with a comma instead of a colon.

    Delete your jQuery selectors, leaving an empty document ready function.       

You can also change the non-CSS properties of HTML elements with jQuery. For example, you can disable buttons.

    When you disable a button, it will become grayed-out and can no longer be clicked.

    jQuery has a function called .prop() that allows you to adjust the properties of elements.

    Here's how you would disable all buttons:

    $("button").prop("disabled", true);

Using jQuery, you can change the text between the start and end tags of an element. You can even change HTML markup.

    jQuery has a function called .html() that lets you add HTML tags and text within an element. Any content previously within the element will be completely replaced with the content you provide using this function.

    Here's how you would rewrite and emphasize the text of our heading:

    $("h3").html("<em>jQuery Playground</em>");
    jQuery also has a similar function called .text() that only alters text without adding tags. In other words, this function will not evaluate any HTML tags passed to it, but will instead treat it as the text you want to replace the existing content with.

    Change the button with id target4 by emphasizing its text.

    View our news article for <em> to learn the difference between <i> and <em> and their uses.

    Note that while the <i> tag has traditionally been used to emphasize text, it has since been adopted for use as a tag for icons. The <em> tag is now widely accepted as the tag for emphasis. Either will work for this challenge.

Now let's remove an HTML element from your page using jQuery.

    jQuery has a function called .remove() that will remove an HTML element entirely.

    Remove the #target4 element from the page by using the .remove() function.
    $("#target4").remove();

Now let's try moving elements from one div to another.

    jQuery has a function called appendTo() that allows you to select HTML elements and append them to another element.

    For example, if we wanted to move target4 from our right well to our left well, we would use:

    $("#target4").appendTo("#left-well");
    Move your target2 element from your left-well to your right-well.

In addition to moving elements, you can also copy them from one place to another.

    jQuery has a function called clone() that makes a copy of an element.

    For example, if we wanted to copy target2 from our left-well to our right-well, we would use:

    $("#target2").clone().appendTo("#right-well");
    Did you notice this involves sticking two jQuery functions together? This is called function chaining and it's a convenient way to get things done with jQuery.

    Clone your target5 element and append it to your left-well.

Every HTML element has a parent element from which it inherits properties.

    For example, the h3 element in your jQuery Playground has the parent element of <div class="container-fluid">, which itself has the parent element of body.

    jQuery has a function called parent() that allows you to access the parent of whichever element you've selected.

    Here's an example of how you would use the parent() function if you wanted to give the parent element of the left-well element a background color of blue:

    $("#left-well").parent().css("background-color", "blue")

When HTML elements are placed one level below another they are called children of that element.
    For example, the button elements in this challenge with the text #target1, #target2, and #target3 are all children of the <div class="well" id="left-well"> element.

    jQuery has a function called children() that allows you to access the children of whichever element you've selected.

    Here's an example of how you would use the children() function to give the children of your left-well element the color blue:

    $("#left-well").children().css("color", "blue")

You've seen why id attributes are so convenient for targeting with jQuery selectors. But you won't always have such neat ids to work with.

    Fortunately, jQuery has some other tricks for targeting the right elements.

    jQuery uses CSS Selectors to target elements. The target:nth-child(n) CSS selector allows you to select all the nth elements with the target class or element type.

    Here's how you would give the third element in each well the bounce class:

    $(".target:nth-child(3)").addClass("animated bounce");
You can also target elements based on their positions using :odd or :even selectors.

    Note that jQuery is zero-indexed which means the first element in a selection has a position of 0. This can be a little confusing as, counter-intuitively, :odd selects the second element (position 1), fourth element (position 3), and so on.

    Here's how you would target all the odd elements with class target and give them classes:

    $(".target:odd").addClass("animated shake");
    Try selecting all the even target elements and giving them the classes of animated and shake. Remember that even refers to the position of elements with a zero-based system in mind.
jQuery can target the body element as well.

    Here's how we would make the entire body fade out: $("body").addClass("animated fadeOut");
