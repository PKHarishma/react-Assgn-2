1. What is NPM?
NPM (Node Package Manager) is a package manager for JavaScript. It allows developers to install, update, and manage dependencies (libraries and tools) that are required in their projects. It also provides a platform for developers to share their own packages with the community.

2. What is Parcel/Vite? Why do we need it?
Parcel and Vite are modern build tools and bundlers used in web development. They handle tasks like bundling JavaScript files, compiling modern JavaScript to older versions for compatibility, optimizing assets (like images and CSS), and more.

Parcel is a zero-configuration bundler, meaning it works out of the box with minimal setup. It automatically detects and configures tools like Babel and PostCSS, and offers features like hot module replacement and tree shaking.
Vite is a build tool that provides a faster and leaner development experience, particularly with frameworks like Vue and React. It uses native ES modules and a development server that provides fast hot module replacement.
Why do we need them? These tools simplify and optimize the development process, making it easier to manage assets, improve build times, and ensure that the final code is optimized for production.

3. What is .parcel-cache?
The .parcel-cache folder is created by Parcel to store cached files that speed up subsequent builds. By caching intermediate build steps, Parcel avoids redundant work, significantly reducing build times.

4. What is npx?
npx is a command-line tool that comes with NPM. It allows you to execute Node.js packages without needing to install them globally. This is useful for running one-off commands or using packages without polluting your global environment.

5. What is the difference between dependencies vs devDependencies?
Dependencies are the packages your project needs to run in production. They are necessary for your application to work.
DevDependencies are the packages that are only needed during the development phase, like testing frameworks, build tools, or linters. They are not included in the production build.
6. What is Tree Shaking?
Tree shaking is a process used in JavaScript bundlers to eliminate dead code (code that is never used). This optimization reduces the final bundle size, making the application faster to load.

7. What is Hot Module Replacement?
Hot Module Replacement (HMR) is a feature that allows modules to be updated in a running application without requiring a full page reload. This speeds up development by preserving the application state, reducing the time it takes to see the changes made to the code.

8. List down your favorite 5 superpowers of Parcel and describe any 3 of them in your own words.
Here are five powerful features of Parcel:

Zero Configuration: Parcel requires no configuration to get started, which makes it incredibly easy for beginners and saves time for experienced developers.
Built-in Support for Multiple Asset Types: Parcel can handle JavaScript, CSS, HTML, images, and more right out of the box without needing additional plugins.
Automatic Code Splitting: Parcel can automatically split your code into smaller bundles, optimizing the loading time of your application.
Hot Module Replacement: As mentioned earlier, HMR allows for real-time updates without full page reloads.
Tree Shaking: Parcel automatically removes unused code, optimizing the final bundle size.
Descriptions:

Zero Configuration: One of the most compelling features of Parcel is its zero-configuration setup. It automatically detects the technologies you're using and configures them for you. This is a massive time-saver and simplifies the development process.
Automatic Code Splitting: Parcel intelligently splits your code into smaller chunks that are loaded on demand. This reduces the initial load time of your application and improves the user experience, especially in large applications.
Tree Shaking: By analyzing your code, Parcel removes any dead or unused code during the build process. This results in a smaller, more efficient bundle, which ultimately speeds up your application.
9. What is .gitignore? What should we add and not add into it?
.gitignore is a file in which you specify files and directories that Git should ignore. This prevents them from being tracked and added to your repository.

What to add:

Files generated by your build process (e.g., dist/, build/)
Local environment files (e.g., .env)
Dependency directories (e.g., node_modules/)
System-specific files (e.g., .DS_Store on macOS, Thumbs.db on Windows)
What not to add:

Files that are required to build or run the application (e.g., package.json)
Source code files and configuration files that should be versioned and shared with others.
10. What is the difference between package.json and package-lock.json?
package.json is the main file that contains metadata about your project, including the list of dependencies and scripts.
package-lock.json is an automatically generated file that records the exact versions of dependencies and their dependencies. It ensures consistent installs across different environments.
11. Why should I not modify package-lock.json?
You should not manually modify package-lock.json because it is auto-generated by NPM to ensure consistent installations. Editing it manually can lead to inconsistencies and potentially break your project when others try to install dependencies.

12. What is node_modules? Is it a good idea to push that on Git?
node_modules is the directory where NPM installs all the packages your project depends on. It’s generally not a good idea to push this directory to Git because:

It’s usually very large, containing potentially thousands of files.
Dependencies can be re-installed using package.json and package-lock.json, making node_modules redundant in version control.
13. What is the dist folder?
The dist folder (short for "distribution") is where the final production build of your project is stored. It contains all the compiled and optimized files that are ready to be deployed to a server.

14. What is browserlists?
browserslist is a tool used in front-end development to specify which browsers you want your code to support. It is used by tools like Babel, Autoprefixer, and others to ensure that your code is compatible with the specified browsers.