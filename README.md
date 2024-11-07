PEMS Web Custom Code

This repository hosts custom CSS and HTML files used for styling and content on the Precision Electric Motors Sales (PEMS) backend. By hosting these files on GitHub, we ensure a centralized and easily maintainable structure, allowing for seamless updates and integration in our web backend.

GitHub Pages is enabled for this repository, so all files can be accessed directly via URLs, making them easy to link and use in your backend application.
Repository Structure

The repository is organized as follows:

Pems-Web-Custom-Code/
├── index.html                 # Main HTML file with links to previews and raw CSS files
├── Header/
│   ├── styles.css             # CSS file for custom header styles
│   └── preview-header.html    # HTML file to preview the header styles
└── Footer/
    ├── footer-styles.css      # CSS file for custom footer styles
    └── preview-footer.html    # HTML file to preview the footer styles
    └── footer.html            # HTML file containing the footer structure

Files Overview

    index.html: The main entry point for the repository, providing links to view previews and raw code for both the header and footer styles.
    Header/styles.css: Contains custom CSS styling for the header section used on PEMS backend pages.
    Header/preview-header.html: A preview page for testing and viewing the header styles in a sample layout.
    Footer/footer-styles.css: Contains custom CSS styling for the footer section used on PEMS backend pages.
    Footer/preview-footer.html: A preview page for testing and viewing the footer styles in a sample layout.
    Footer/footer.html: Contains the HTML structure for the footer, which can be embedded directly in the backend.

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

3. Embedding the Footer HTML

To directly include the footer HTML structure from GitHub in your backend, you can use JavaScript to fetch and embed it.
Footer HTML Code (footer.html)

The following HTML is stored in footer.html within this repository:


<footer>
    <div>
        <a href="http://www.pemsmotors.com/">
            Precision Electric Motors Sales
            <br>© 2024            
        </a>
        <a href="https://www.pemsmotors.com/digital-resources">
            Digital
            <br>Resources
        </a>
        <a href="http://www.pemsmotors.com/contact/">
            Contact
            <br>Us
        </a>
        <a href="http://www.pemsmotors.com/locations/">
            Locations
        </a>
        <a href="http://www.pemsmotors.com/careers">
            Careers
        </a>
        <a href="http://www.websitepipeline.com/">
            Ecommerce & ERP Integration
            <br>by Website Pipeline
        </a>
    </div>
</footer>

Embedding Footer HTML in Your Backend

    Create a div in your backend HTML where the footer will be inserted:

<div id="footer-container"></div>

Add JavaScript to fetch the HTML from GitHub and insert it into the div:

    <script>
      fetch('https://pems-motors.github.io/Pems-Web-Custom-Code/Footer/footer.html')
        .then(response => response.text())
        .then(data => document.getElementById('footer-container').innerHTML = data);
    </script>

This JavaScript code fetches footer.html and injects it into the footer-container div. This approach keeps your backend code clean and allows for easy updates to the footer content by simply updating the HTML file in this repository.
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