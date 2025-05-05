<p align="center">
  <a href="https://github.com/TheAcharya/MarkerData"><img src="https://raw.githubusercontent.com/TheAcharya/MarkerData-Website/refs/heads/main/docs/assets/md-pagemaker.png">
  <h1 align="center">Pagemaker</h1>
</p>


<p align="center"><a href="https://github.com/TheAcharya/MarkerData-Pagemaker/blob/main/LICENSE"><img src="http://img.shields.io/badge/license-MIT-lightgrey.svg?style=flat" alt="license"/></a>&nbsp;<a href="https://github.com/TheAcharya/MarkerData-Pagemaker"><img src="https://img.shields.io/badge/platform-macOS-lightgrey.svg?style=flat" alt="platform"/></p>

Pagemaker is a lightweight module designed to bridge a key gap in the Marker Data toolset: the ability to generate and export PDFs from [Final Cut Pro](https://www.apple.com/final-cut-pro/)'s Marker metadata with images. Originally, Marker Data lacked native support for PDF export. With the introduction of the Pagemaker module, this limitation has been thoughtfully addressed.

Starting with Marker Data version 1.2.0, **Marker Data now allows users to load a data set, extracted via Notion or Airtable using Marker Data's Extraction Profiles and generate a dynamic, visual web gallery. Once the Data Set is loaded, users can explore its contents through a searchable and filterable interface. Selected items can then be exported into a cleanly formatted, print-ready PDF, making it easy to share with clients, team members, or maintaining as project archives.

## Maintenance

Pagemaker was developed as a side project—born from curiosity and a spirit of experimentation. While it is functional and stable, it is not under active development. No additional features or paper sizes are planned, and ongoing maintenance will be minimal. That said, if any bugs or critical issues arise within the existing codebase, we will make a best-effort attempt to resolve them.

## Project Structure

The entire application is currently encapsulated within a single HTML file. While this may diverge from conventional development practices—which typically advocate for separating HTML, CSS, and JavaScript—it was an intentional design decision.

After careful consideration, I have opted for a unified file structure to ensure easier maintenance and smoother integration with Marker Data’s WebKit View. This approach also simplifies the process of loading the code into AI-assisted tools and platforms, which often benefit from having the full context in a single file.

To support readability and future enhancements, the code has been thoroughly documented with comment blocks and inline explanations. The intent is to make the logic and flow as transparent and accessible as possible.

## Credits

Created by [Vigneswaran Rajkumar](https://bsky.app/profile/vigneswaranrajkumar.com)

## License

Licensed under the MIT license. See [LICENSE](https://github.com/TheAcharya/MarkerData-Pagemaker/blob/main/LICENSE) for details.

## Reporting Bugs

For bug reports, feature requests and suggestions you can create a new [issue](https://github.com/TheAcharya/MarkerData-Pagemaker/issues) to discuss.

## Contribution

Community contributions are welcome and appreciated. Developers are encouraged to fork the repository and submit pull requests to enhance functionality or introduce thoughtful improvements. However, a key requirement is that nothing should break—all existing features, behaviours theme and styling must remain fully functional and unchanged. Once reviewed and approved, updates will be merged into the main branch and made available within the Marker Data.