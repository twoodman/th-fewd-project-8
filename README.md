### Project 8 for Treehouse FEWD Course
----

#### Accessibility Refactor

Take a set of interlinked pages that suffer from various accessibility
flaws and refine and update them so they are accessible and pass an accessibility
validator(s)'s automated checks and a human's check.


##### To Run:
- Download or clone repo
- Open index.html in browser


##### Or:
- http://twoodman.github.io/th-fewd-project-8


##### Tested In:
Chrome 53 on Mac OS Sierra
Firefox 49 on Mac OS Sierra
Safari 10 on Mac OS Sierra

##### To Do:
- FOLLOWING DONE IN:
  - ✔️ index.html
  - ✔️ survey.html
  - ✔️ tour.html
----
- ✔️ REFACTOR CSS TO SASS
- ✔️ LANGUAGE
  - Specify lang w/ lang attr in html tag
- ✔️ DESIGN
  - Foreground / background text have [sufficient contrast](http://leaverou.github.com/contrast-ratio/)
- ✔️ DOCUMENT STRUCTURE
  - Ensure heading elements (h1) are used to provide hierarchal structure to page content
  - Look for p tags w/ class 'heading' these should be changed to help assist screen readers
- ✔️ IMAGES
  - Replace text in banner w/ HTML text to roughly match mockup layout
  - Add alt tags to imgs
  - Make decorative images in tour.html page have empty alt attr, attr=''
- ✔️ LINKS
  - Ensure links are visually distinct
  - Add hover state to links
  - Ensure image link icons in footer have text describing the link, but make invisible to viewer. Use either alt text or css to hide text.
- ✔️ TABLE
  - Create a table for the tour dates info using td for table data cells and th for table header cells
  - Ensure table has scope and caption elements
- ✔️ FORM
  - Ensure form elements have styled focus states (:focus pseudo)
  - Add labels for form controls
  - Ensure all labels have 'for' attr, match 'for' and 'id' values
  - Group form elements with fieldset
  - Add legend to describe grouping
  - Ensure select field options in alphabetical order
  - Make sure you can use keyboard to select from select field drop down
- ✔️ CHECKING CODE
  - Check code using Chrome Accessibility extension (chrome) and Fangs extension (firefox)

  *Fangs was last updated in 2010 and I actually can't seem to launch it, it doesn't appear in tools. According to comments it also doesn't support html5 tags and is buggy, so unfortunately going to pass on Fangs. Perhaps this should be removed from the project page's suggestions.*

  - Instead I checked the site using ChromeVox, seemed OK to me.

  - I also downloaded and checked the site over with a Mac app called Sim Daltonism, it lets you view things as those with deuteranopia, deuteranomaly, protanopia, protanomaly, tritanopia, tritanomaly, monochromacy, and partial monochromacy do. The site held up on all of them, and had easily distinguishable elements.

  - Run code through [accessibility validator](http://achecker.ca/checker/index.php#)
    - I checked for WCAG 2.0 Level AAA, no problems
  - Check code against [accessibility checklist](http://a11yproject.com/checklist.html)
    - ✔️Checked ✔️off ✔️everything ✔️that ✔️applied
- ✔️ VALIDATING CODE
  - Run HTML through [validator](https://validator.w3.org/#validate_by_input)
    - mostly telling me that role attributes weren't necessary, ignored that
    - got pipe character encoding error, so replaced it to satisfy the validation gods
    - caught some of my dumb mistakes, like leaving rogue closing tags, and my table header scope blunder where I put "Location" in a scope attribute instead of "col" when it was actually just supposed to be that headers text.
  - Run CSS through [validator](https://jigsaw.w3.org/css-validator/#validate_by_input)
    - no errors, gave vendor extension warnings for compass mixins though

##### Exceeds Expectations:
- ✔️ Add aria-landmarks roles attributes to sections of page
  - Need 3 per page, using most appropriate role value for the content of container
  - footer section example:
  ```
    <footer role="contentinfo">
  ```
- ✔️ Use aria-describedby to add a description of what the submit form button does when clicked and provide more information about parts of the form
  - example:
  ```
    <label for="password">Choose a password</label>
      <input type="password" id="password" aria-describedby="hint" ...>

      <p id="hint">Your password must be at least 10 characters in length.
      It must contain a mixture of upper and lower case letters,
      numbers and punctuation marks.</p>
  ```
