
# Form Sync Integration Example

This repository provides an example of how to integrate the `Form Sync` product into a simple HTML form. The example includes a form where users can input information, submit the form, and have the data captured by the `Form Sync` service for further processing.

## Getting Started

To use this example, follow these steps:

1. Include the `Form Sync` script in your HTML file.
2. Create a form with input fields and a submit button.
3. Ensure that each form input field has a `name` attribute.

### Prerequisites

- Basic knowledge of HTML and JavaScript.
- An account with `Form Sync` to capture and view form submissions. [Register here](https://form-sync.cloud/register).

## Installation

Add the `Form Sync` script tag before the closing `</body>` tag of your HTML file:

```html
<script src="https://form-sync.cloud/js/save-data.js"></script>
```

Initialize `Form Sync` with the form class and optional configuration parameters:

```javascript
FormSync('.your-form-class-name', {
    thankYouMsg: 'my Custom MSG',
});
```

## Demo

Here is a demo example of how to use the `Form Sync` script with a simple HTML form:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Sync Integration Example</title>
</head>
<body>
    <form method="POST" class="form-sync">
        <input type="text" name="name" id="name" placeholder="Name" required />
        <input type="text" name="email" id="email" placeholder="Email" required />
        <input type="text" name="phone" id="phone" placeholder="Phone" required />
        <input type="text" name="message" id="message" placeholder="Message" required />
        <input type="submit" value="Submit" id="submit">
    </form>

    <script src="https://form-sync.cloud/js/save-data.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            FormSync('.form-sync', {
                thankYouMsg: 'my Custom MSG',
            });
        });
    </script>
</body>
</html>
```

## Notes

- The `Form Sync` script automatically captures the data from the form fields when the form is submitted.
- You can customize the `thankYouMsg` parameter to display a custom message after form submission.

## Registration

To start using `Form Sync`, you need to create an account. [Register here](https://form-sync.cloud/register) to get started.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the `Form Sync` team for providing the data synchronization service.
