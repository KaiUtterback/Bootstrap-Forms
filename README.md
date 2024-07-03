# Bootstrap Forms Project

## Overview

This project demonstrates the use of Bootstrap to create visually appealing and responsive form layouts. It includes multiple form styles such as multi-column, inline, and stacked forms, all enhanced with floating labels and real-time validation feedback.

## Features

- **Multi-Column Form Layout**: Uses Bootstrap's grid system to arrange form fields in two columns on medium and larger devices.
- **Inline Contact Form**: Displays input fields and a submit button aligned horizontally for a compact layout.
- **Stacked Form Layout**: Provides a stacked layout with labels above input fields for better readability and accessibility.
- **Floating Labels**: Implements floating labels for a modern touch to input fields.
- **Form Validation**: Incorporates Bootstrap's validation classes to provide real-time feedback for invalid and valid inputs.
- **Hero Section**: A visually engaging hero section with the title "Bootstrap Forms!" to highlight the purpose of the page.

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/bootstrap-forms-project.git
   ```

2. Navigate to the project directory:
   ```sh
   cd bootstrap-forms-project
   ```

3. Open `index.html` in your web browser to view the forms.

## Usage

### Multi-Column Form Layout

- **Description**: Arranges input fields in two columns using Bootstrap's grid system.
- **Usage**: Ideal for forms requiring a balanced layout, such as registration or profile update forms.
- **Code Snippet**:
  ```html
  <div class="form-section">
    <h2>Multi-Column Form Layout</h2>
    <form class="needs-validation" novalidate>
      <div class="form-row">
        <div class="form-group col-md-6">
          <div class="form-floating mb-3">
            <input type="text" class="form-control" id="inputFirstName" placeholder="First Name" required>
            <label for="inputFirstName">First Name</label>
            <div class="invalid-feedback">Please provide your first name.</div>
            <div class="valid-feedback">Looks good!</div>
          </div>
        </div>
        <div class="form-group col-md-6">
          <div class="form-floating mb-3">
            <input type="text" class="form-control" id="inputLastName" placeholder="Last Name" required>
            <label for="inputLastName">Last Name</label>
            <div class="invalid-feedback">Please provide your last name.</div>
            <div class="valid-feedback">Looks good!</div>
          </div>
        </div>
      </div>
      <div class="form-row">
        <div class="form-group col-md-6">
          <div class="form-floating mb-3">
            <input type="email" class="form-control" id="inputEmail" placeholder="Email" required>
            <label for="inputEmail">Email</label>
            <div class="invalid-feedback">Please provide a valid email address.</div>
            <div class="valid-feedback">Looks good!</div>
          </div>
        </div>
        <div class="form-group col-md-6">
          <div class="form-floating mb-3">
            <input type="tel" class="form-control" id="inputPhone" placeholder="Phone" required>
            <label for="inputPhone">Phone</label>
            <div class="invalid-feedback">Please provide a valid phone number.</div>
            <div class="valid-feedback">Looks good!</div>
          </div>
        </div>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
  </div>
  ```

### Inline Contact Form

- **Description**: Aligns input fields and the submit button horizontally for a compact layout.
- **Usage**: Suitable for contact forms or quick input forms.
- **Code Snippet**:
  ```html
  <div class="form-section">
    <h2>Inline Contact Form</h2>
    <form class="form-inline needs-validation" novalidate>
      <div class="form-group mb-2">
        <label for="inputName" class="sr-only">Name</label>
        <input type="text" class="form-control" id="inputName" placeholder="Name" required>
        <div class="invalid-feedback">Please provide your name.</div>
        <div class="valid-feedback">Looks good!</div>
      </div>
      <div class="form-group mx-sm-3 mb-2">
        <label for="inputEmailInline" class="sr-only">Email</label>
        <input type="email" class="form-control" id="inputEmailInline" placeholder="Email" required>
        <div class="invalid-feedback">Please provide a valid email address.</div>
        <div class="valid-feedback">Looks good!</div>
      </div>
      <button type="submit" class="btn btn-primary mb-2">Submit</button>
    </form>
  </div>
  ```

### Stacked Form Layout

- **Description**: Provides a stacked layout with labels above input fields for better readability and accessibility.
- **Usage**: Ideal for comprehensive forms with multiple fields, such as surveys or application forms.
- **Code Snippet**:
  ```html
  <div class="form-section">
    <h2>Stacked Form Layout</h2>
    <form class="needs-validation" novalidate>
      <div class="form-group">
        <div class="form-floating mb-3">
          <input type="text" class="form-control" id="inputFirstNameStacked" placeholder="First Name" required>
          <label for="inputFirstNameStacked">First Name</label>
          <div class="invalid-feedback">Please provide your first name.</div>
          <div class="valid-feedback">Looks good!</div>
        </div>
      </div>
      <div class="form-group">
        <div class="form-floating mb-3">
          <input type="text" class="form-control" id="inputLastNameStacked" placeholder="Last Name" required>
          <label for="inputLastNameStacked">Last Name</label>
          <div class="invalid-feedback">Please provide your last name.</div>
          <div class="valid-feedback">Looks good!</div>
        </div>
      </div>
      <div class="form-group">
        <div class="form-floating mb-3">
          <input type="email" class="form-control" id="inputEmailStacked" placeholder="Email" required>
          <label for="inputEmailStacked">Email</label>
          <div class="invalid-feedback">Please provide a valid email address.</div>
          <div class="valid-feedback">Looks good!</div>
        </div>
      </div>
      <div class="form-group">
        <div class="form-floating mb-3">
          <input type="tel" class="form-control" id="inputPhoneStacked" placeholder="Phone" required>
          <label for="inputPhoneStacked">Phone</label>
          <div class="invalid-feedback">Please provide a valid phone number.</div>
          <div class="valid-feedback">Looks good!</div>
        </div>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
  </div>
  ```

## Custom Validation

- **Description**: Uses Bootstrap's validation classes to provide real-time feedback for invalid and valid inputs.
- **Code Snippet**:
  ```javascript
  <script>
    // Example starter JavaScript for disabling form submissions if there are invalid fields
    (function() {
      'use strict';
      window.addEventListener('load', function() {
        // Fetch all the forms we want to apply custom Bootstrap validation styles to
        var forms = document.getElementsByClassName('needs-validation');
        // Loop over them and prevent submission
        var validation = Array.prototype.filter.call(forms, function(form) {
          form.addEventListener('submit', function(event) {
            if (form.checkValidity() === false) {
              event.preventDefault();
              event.stopPropagation();
            }
            form.classList.add('was-validated');
          }, false);
        });
      }, false);
    })();
  </script>
  ```

## Demo

To see the forms in action, open `index.html` in your web browser.

## Contributing

Feel free to submit issues and pull requests if you find any bugs or have suggestions for improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
