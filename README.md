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


##### To Do:
- LANGUAGE
  - Specify lang w/ lang attr in html tag
- DESIGN
  - Foreground / background text have [sufficient contrast](http://leaverou.github.com/contrast-ratio/)
- DOCUMENT STRUCTURE
  - Ensure heading elements (h1) are used to provide hierarchal structure to page content
  - Look for p tags w/ class 'heading' these should be changed to help assist screen readers
- IMAGES
  - Replace text in banner w/ HTML text to roughly match mockup layout
  - Add alt tags to imgs
  - Make decorative images in tour.html page have empty alt attr, attr=''
- LINKS
  - Ensure links are visually distinct
  - Add hover state to links
  - Ensure image link icons in footer have text describing the link, but make invisible to viewer. Use either alt text or css to hide text.
- TABLE
  - Create a table for the tour dates info using td for table data cells and th for table header cells
  - Ensure table has scope and caption element
- FORM
  - Ensure form elements have styled focus states (:focus pseudo)
  - Add labels for form controls
  - Ensure all labels have 'for' attr, match 'for' and 'id' values
  - Group form elements with fieldset
  - Add legend to describe grouping
  - Ensure select field options in alphabetical order
  - Make sure you can use keyboard to select from select field drop down
- CHECKING CODE
  - Check code using Chrome Accessibility extension (chrome) and Fangs extension (firefox)
  - Run code through [accessibility validator](http://achecker.ca/checker/index.php#)
  - Check code against [accessibility checklist](http://a11yproject.com/checklist.html)
- VALIDATING CODE
  - Run HTML through [validator](https://validator.w3.org/#validate_by_input)
  - Run CSS through [validator](https://jigsaw.w3.org/css-validator/#validate_by_input)

##### Exceeds Expectations:
- Add aria-landmarks roles attributes to sections of page
  - Need 3 per page, using most appropriate role value for the content of container
  - footer section example:
  ```
    <footer role="contentinfo">
  ```
- Use aria-describedby to add a description of what the submit form button does when clicked and provide more information about parts of the form
  - example:
  ```
    <label for="password">Choose a password</label>
      <input type="password" id="password" aria-describedby="hint" ...>

      <p id="hint">Your password must be at least 10 characters in length.
      It must contain a mixture of upper and lower case letters,
      numbers and punctuation marks.</p>
  ```
