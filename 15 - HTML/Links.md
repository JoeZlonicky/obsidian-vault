### Descriptions
Links can be made using `<a> </a>` tags. The actually functionality of the element depends on the attributes added:
* `href="..."` sets the destination and is required for the element to show as a link
* `target="..."` tells the browser if the link should be opened in a new tab/window. The default value is `_self` which opens in the current tab. `_blank` opens in a new window.
* `rel="nopener"` prevents the opened link from gaining access to the webpage from which it was opened. This prevents phishing attacks, known as tab-nabbing.
* `rel="noreferrer"` prevents the opened link from knowing which webpages or resource has a link to it. It also includes the `noopener` behavior.

Links to other websites are called absolute links and follow the pattern of `protocol://domain/path`.

Links to pages within the same website are called relative links and can be specified simply with `./path/to/page.html`.