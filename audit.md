# Audit Performance

In this documentation, we’re going to identify the common problems that might affect the website’s performance, also we’re going to provide suggestions for a better user experience and improve page load performance.

We're going to use *Chrome DevTools* to identify these problems and to find ways to make the page load faster.

## [Todolistme.net](http://todolistme.net/) - Competitor's website performance

| ![Audit todolistme.net](https://github.com/msharafjr/p8-todo-list-app/blob/master/screenshoots/audit-todolistme.png) | 
|:--:| 
| *Audit Result* |

### Metrix

- The overall performance score is **39%**.
- First content paint **1.7 s**
- Time to interactive **11.9 s**
- First meaningful paint **2.9 s**
- Time to load is **1.9 s**
- Max Potential First Input Delay **1,310 ms**

### Concerns

- Total number of requests is **96** request, with transfer size **1.0 MB**.
- Images only has **33** requsts total.
- Some JavaScript files are not minified.
- There are **render-blocking** resources that need to be eliminated.

### Opportunities

- Using **HTTP/2** over **HTTP/1.1**, which offers many benfites and will make the application way faster.
- Using **CSS Image Sprites** to collect small images into a single image.
- Minify **jquery-ui.js** file gives us a potential savings **44 KB**.
- Move critical code to an inline script, we can keep non-critical code with **async** or **defer** attribute, and unused code should be deleted.

### Additional Improvements for Accessibility & Best Practices

- Stop using `document.write()`, it could delay the page load by tens of seconds.
- A third-party library `jQuery@2.2.4` may contain known security vulnerabilities that are easily identified and exploited by attackers.
- Resolve all the problems that is logged to the console.
- Include a `<meta name="viewport">` tag with `width` or `initial-scale` to optimize the app for mobile screens.
- All images tags should have `alt`(alternate text) attribute.

| ![Usege Visualization & Unused Bytes](https://github.com/msharafjr/p8-todo-list-app/blob/master/screenshoots/coverage-todolistme.png) |
|:--:|
| *Usege Visualization & Unused Bytes* |

<br />
<hr />
<br />

## Todo-list-app - Our website's performance

| ![Audit todo-list-app](https://github.com/msharafjr/p8-todo-list-app/blob/master/screenshoots/audit-todo-list-app.png) |
|:--:|
| *Audit Result* |

### Metrix

- The overall performance score is **99%**.
- First content paint **1.9 s**
- Time to interactive **2.0 s**
- First meaningful paint **1.9 s**
- Time to load is **1.88 s**
- Max Potential First Input Delay **100 ms**

### Concerns

- Total number of requests is **12** request, with transfer size **82 KB**.
- Some JavaScript/Stylesheet files are not minified.
- There are **render-blocking** resources that need to be eliminated.

### Opportunities

- Using **HTTP/2** over **HTTP/1.1**, which offers many benfites and will make the application way faster.
- Minify JS & CSS files gives us a potential savings **920 ms**.
- Move critical code to an inline script, we can keep non-critical code with **async** or **defer** attribute, and unused code should be deleted.

### Additional Improvements for Accessibility & Best Practices

- Form elements `input.new-todo` do not have associated labels.
- Resolve all the problems that is logged to the console.

| ![Usege Visualization & Unused Bytes](https://github.com/msharafjr/p8-todo-list-app/blob/master/screenshoots/coverage-todo-list-app.png) |
|:--:|
| *Usege Visualization & Unused Bytes* |
