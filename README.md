PEMS Web Custom Code

This repository hosts custom CSS and HTML files used for styling and content on the Precision Electric Motors Sales (PEMS) backend. By hosting these files on GitHub, we ensure a centralized and easily maintainable structure, allowing for seamless updates and integration in our web backend.

GitHub Pages is enabled for this repository, so all files can be accessed directly via URLs, making them easy to link and use in your backend application.
Usage
1. Accessing the Previews

To view how the custom header and footer styles will appear, use the following links:

    Header Preview: Header/preview-header.html
    Footer Preview: Footer/preview-footer.html

Each preview file includes sample HTML content that applies the CSS styling to give you a live view of how it would look in your backend.
2. Linking the CSS Files in Your Backend

To apply these styles directly in your backend application, link to the raw CSS files hosted on GitHub Pages.
Header CSS

Add the following link to your backend HTML to include the custom header styling:

<link rel="stylesheet" href="https://pems-motors.github.io/Pems-Web-Custom-Code/Header/styles.css">

Footer CSS

Add the following link to your backend HTML to include the custom footer styling:

<link rel="stylesheet" href="https://pems-motors.github.io/Pems-Web-Custom-Code/Footer/footer-styles.css">

3. Adding Code to the Backend Custom Header Section

To use the custom header styles in your backend’s custom header section, include the following code. This uses @import within a <style> tag to load the CSS from GitHub:

<style>
  /* Import the header styles from GitHub */
  @import url("https://pems-motors.github.io/Pems-Web-Custom-Code/Header/styles.css");
</style>

This approach allows the header CSS to load directly from GitHub Pages, automatically updating with any changes made to styles.css.
4. Adding Code to the Backend Custom Footer Section

To add both the styling and HTML for the footer in your backend’s custom footer section, include the following:

<!-- Load the footer styles from GitHub -->
<style>
  @import url("https://pems-motors.github.io/Pems-Web-Custom-Code/Footer/footer-styles.css");
</style>

<!-- Fetch and insert the footer HTML content from GitHub -->
<script>
  fetch('https://pems-motors.github.io/Pems-Web-Custom-Code/Footer/footer.html')
    .then(response => response.text())
    .then(data => document.getElementById('footer-container').innerHTML = data)
    .catch(error => console.error('Error loading footer:', error));
</script>

Additionally, ensure there is a placeholder div on your backend page where the footer HTML will be injected:

<div id="footer-container"></div>

Embedding the Footer HTML Directly

To directly include the footer HTML structure from GitHub in your backend without modifying the main page, this JavaScript fetches the HTML from GitHub Pages and injects it into the footer-container div. Any changes to footer.html will automatically update in the backend.
Local Development and Testing

To make local changes and test them before pushing to GitHub, follow these steps:

    Clone the Repository:

    git clone https://github.com/PEMS-Motors/Pems-Web-Custom-Code.git
    cd Pems-Web-Custom-Code

    Open in VSCode and use the Live Server extension to preview index.html and other HTML files in your browser.

    Edit the CSS or HTML files as needed. The preview files (preview-header.html and preview-footer.html) allow you to see the impact of changes on sample content.

    Commit and Push Changes: Once you’re satisfied with the changes, commit and push them to GitHub. The updates will be available through GitHub Pages and linked automatically in your backend.

Notes

    Caching: GitHub Pages may cache files, so changes might take a few minutes to reflect. Clear your browser cache if you don’t see updates immediately.
    GitHub Pages URL: The base URL for GitHub Pages is:

    https://pems-motors.github.io/Pems-Web-Custom-Code/

    Use this URL to access all files hosted in this repository.

Support

If you have questions or need further assistance, please reach out to the PEMS development team.

This setup enables you to manage, test, and update your backend CSS and HTML assets directly from GitHub, ensuring a streamlined and maintainable workflow.