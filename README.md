# Portfolio
## Technical Requirment
- use Jtest for all components
- use Firebase for contact us 
- use axios to get repos from github api


## Design instructions
https://www.figma.com/blog/how-to-wireframe/

## Porfolio Technical Guide

**Github**

- We will use Github to collaborate, review and manage the projects. We are going to follow this [article](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) for the workflow we are going to use.

**Github project management**

- Github project management helps project managers and developers coordinate, track, and update their work in one place, so projects stay transparent and on schedule, learn more about [github project management](https://github.com/features/project-management/)

**GithubAction**

- Continuous integration “CI” is the practice of merging all developers' working copies to a shared mainline several times a day, learn more about CI in this [article](https://www.atlassian.com/continuous-delivery/continuous-integration) and this [wikipedia page](https://en.wikipedia.org/wiki/Continuous_integration).


**Netlify**

- Netlify is a tool that offers hosting and serverless backend services for web applications and static websites just by pushing the code to the repo, learn more about [Netlify](https://www.netlify.com/)
- I would suggest either making a Re:Coded account that pays for build time or having one student be responsible for hosting their site
- Make sure to turn off Netlify deploy for merge requests (this will consume too much build time).

**Yarn**

- Yarn is a package manager for your code. It allows you to use and share code with other developers from around the world. Yarn does this quickly, securely, and reliably so you don't ever have to worry. Learn more about [yarn](https://yarnpkg.com/).
- Yarn is pretty much the same as npm but much more convenient these days.

**Jest**

- Jest is a delightful JavaScript Testing Framework with a focus on simplicity, learn more about [Jest](https://jestjs.io/)

**Firebase**

- Firebase is Google's mobile and web application development platform, learn more about [firebase](https://firebase.com/)

Repository Setup

- You will be provided with the link for your projects repo on github
- A team member should fork it and set it up, create react app, add eslint and prettier config and all other required packages e.g. firebase if you’re using firebase, set the directories structure, then push the code back.
- Add CircleCI and Netlify config to the repo, this is an [example](https://medium.com/swlh/an-example-ci-process-for-react-apps-with-docker-2247171a218)**.**

Project structure

- Use `create-react-app` for the boilerplate react app.

- depending on what flow to take
    - Follow the component container pattern, so your two main folders inside the `src` will be the `components` folder that will contain your components and `containers` that will contain container components. *You can read more about container components [here](https://reactpatterns.com/#container-component) or you can ask you team leader about it for more clarity.*
    - similar concept you can use the component page 
    take a look [here](https://blog.bitsrc.io/structuring-a-react-project-a-definitive-guide-ac9a754df5eb)

- Use `scss` instead of css if you going with `react-bootstrap`
- You can use `postcss` if you are going with another library that uses something like `tailwind`
- Global style variables will be inside a `style` folder inside the `src` inside a `_variables.scss.` If you are using `react-bootstrap` this can come in handy!
- The main folder names inside the `src` should be lower case like `components` and `container or pages` other folders inside them should be TitleCase like `ProgressBar` and files inside these folder will be TitleCase too like `ProgressBar.js.` If you need styles then add them with the same `.js` file name like `ProgressBar.scss`

Your project hierarchy should look something similar to this:

```
.
├── src
	├── components
		├── ProgressBar
			├── ProgressBar.js
			├── ProgressBar.scss
	├── containers
		├── About
				├── ContactForm.js
				├── About.js
	├── style
		├── _variables.scss
```

- All dependencies inside the `package.json` should be used in the project.
- It's recommended to use Yarn to install the packages.
- General use images should be inside a folder inside `src` under `images` and try to use `svg` as much as possible. Component specific images should be under their folders.
- You should have prettier extension installed and make sure your code is well formatted before submitting it.
- Test files will reside under the `test` folder inside the `src` and the extension is `.test.js`

Git

**Pull Requests**

- Go to the issues board and create a new issue with the task assigned to you.
- Assign the issue to yourself so others know who is working on this issue.
- Create a new pull request from that issue and also assign it to yourself, Github will automatically create a branch for you and give you instructions how to check it out.
- After finishing the work, push your code and assign the team leader on that pull request so they can review the code.

**Commit Message Format**

Each commit message consists of a **header**, a **body** and a **footer**. The header has a special format that includes a **type** and a **subject**:

```
<type>: <subject>
<BLANK LINE>
<body>
```

The **header** is mandatory, while the **body** is optional but highly encouraged.

**Type**

Must be one of the following:

- **Build**: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
- **CI**: Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
- **Doc**: Documentation only changes
- **Feat**: A new feature
- **Fix**: A bug fix
- **Perf**: A code change that improves performance
- **Refactor**: A code change that neither fixes a bug nor adds a feature
- **Style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- **Test**: Adding missing tests or correcting existing tests

**Subject**

The subject contains a succinct description of the change:

- use the imperative, present tense: “change” not “changed” nor “changes”
- don’t capitalize the first letter
- no dot (.) at the end

**Body**

Just as in the **subject**, use the imperative, present tense: “change” not “changed” nor “changes”. The body should include the motivation for the change and contrast this with previous behavior.

- There is a really good programming principle that we will focus on during our work like SOLID and KISS. *You can read more about these principles [here](https://github.com/seyna/awesome-programming-principles).*

The Code

- The code should be totally clean and checked line by line before committing and pushing.
- You shouldn't leave any unnecessary comments in the code.
- Don't leave any logs inside the code.
- All variables should be `const` except for specific cases where you will need to use `let`
- Variables should use camelCase naming convention
- CSS classes should follow BEM naming convention. *You can find more about it [here](http://getbem.com/naming/).*
- Leave only one empty line between CSS classes. This also goes for different purpose code blocks (like `imports` and variables under it).
- Make sure your naming is right and not confusing i.e. the `Navbar` shouldn't be named `header` or when you fetch `movies` your function should return `movies` not `data`
- Make sure you clean your imported modules or files that you don't use before committing. The same goes for any variable, function or piece of code not used.
- Don't repeat yourself (DRY). Make sure the code you write is reusable and reduce repetition of information of all kinds. For example, don't write two functions that do the same or almost the same job. R*ead more about DRY [here](https://en.wikipedia.org/wiki/Don't_repeat_yourself).*
- There is a really good programming principle that we will focus on during our work like SOLID and KISS. *You can read more about these principles [here](https://github.com/seyna/awesome-programming-principles).*


Required Readings

- [Google Code Review (overview)](https://google.github.io/eng-practices/review/)
- [Google Code Review (developer)](https://google.github.io/eng-practices/review/developer/)
- [Google Code Review (reviewer)](https://google.github.io/eng-practices/review/reviewer/)
- [Magic numbers](https://www.pluralsight.com/tech-blog/avoiding-magic-numbers/)


Testing

Why test?

There are many reasons to have automated tests in your repository, which are covered in the required readings below. Some of the salient ones:

- **Code safety:** In addition to simply knowing that the code works, developers feel safe changing other people's code and knowing what will happen; if something is changed badly, a test will break.
- **Ease of review:** When reviewing a merge request, the reviewer can understand exactly what was changed by looking at the tests
- **Self-documentation:** Tests are a form of self-documentation on what the expected behavior of the code is.

The Process

Ideally, every code review should have a test. With the exception of boilerplate code, **no code reviews for new components will be accepted without a corresponding test file.**

In general, there are two types of tests, which you will be asked to read about in the required readings.

- **Snapshot tests:** DOM structure testing
- **Functionality tests:** testing functionality, such as "if this is clicked, then X happens"

At bigger companies, you will often reach a point where this statement is almost true: "it is impossible to change a line of code without breaking a test." As you are now familiar with through your projects, it can take only a single wrong line of code to bring down an application.

You may ask: "Isn't that a bit ridiculous? *Every* line of code?" Consider this: how much money does a company like [Facebook or Google lose for every minute of time that it's down](https://venturebeat.com/2013/08/16/3-minute-outage-costs-google-545000-in-revenue/)?

And for that reason, as the product grows bigger, we want to ensure every line of code is working.

As you will learn, writing tests is very time-consuming -- often it takes longer than writing the code itself. For your projects, the requirements will be more lax; however, getting into the habit of thinking about testing will be important for your growth as a developer. What could go wrong with my code? What cases should I be thinking about? Will someone else feel safe changing my code?

Required Readings

- [What is the purpose of unit testing?](http://softwaretestingfundamentals.com/unit-testing/)
- [What makes a good unit test?](https://stackoverflow.com/questions/61400/what-makes-a-good-unit-test)
- [React Testing Docs](https://reactjs.org/docs/testing.html)
- [React Snapshot Testing](https://jestjs.io/docs/en/snapshot-testing)
- [React Testing Library](https://testing-library.com/docs/react-testing-library/intro)

## Portfolio guide
Remember that you portfolio is great way to build your brand as a competent professional, especially in a new field. Your website / portfolio is a representation of what you are capable of.

Having an excellent personal website provides you with a powerful tool to communicate with the world at large (including potential employers and colleagues) highlights your experience and skills, and generates credibility for yourself and your brand as a professional. Your website/portfolio is a representation of what you are currently capable of, and the future direction as a professional you’re headed towards. As newer developers, it's also your ticket to a job, even if you don't have the traditional work experience on your CV.

While there are limitless ways with which you can approach designing and producing your site, it’s important to consider what a potential employer looks for when they look at your portfolio. Below we discuss some key steps and components to be mindful of as you proceed in building your site.

- Beyond the content, an attractive and dynamic design that engages your visitors and keeps them staying longer is key. Make sure that whatever design you go with, the crucial information (listed below) is visible and organized. Sometimes, simple is stronger!
- Think about the purpose of the site. Is it to get noticed? Do you have freelance services you'd like to promote and consequently get clients? Consider what you can include to truly personalize your visitors’ experience, so they can begin to connect with you in meaningful ways. This will also help you define what sections you need to build out more / less.
- **“About” Page/Section**: This can be the same bio you currently use on your resume and/or LinkedIn profile page, so start with that as a placeholder. Consider eventually expanding your website bio to draw visitors deeper into your personal story, vision, and viewpoint about coding: what it means to you and how it impacts you as a professional. For inspiration, read [this article on writing a great bio.](https://www.fastcompany.com/3007103/art-writing-your-own-bio-how-toot-your-horn-without-sounding-blowhard)
    - I would also recommend either embedding your resume on your portfolio, on or near the "About" section. Alternatively, you can "deconstruct" your resume and essentially make it multiple sections of your website ("Education", "Work History", etc.)
- **Technical Projects:** Outline the projects you are most proud of, whether personal, professional, contest, hackathon, or class projects. If you choose a bootcamp project, *do not emphasize that it is coming from a bootcamp*; simply treat it like a personal project.
    - There is flexibility in how you talk about projects. I would always have at least a couple lines describing what the project is and **why you built this project.** If you have time, you can go full-out and talk about your process, challenges, learnings. ([Here's an example](https://www.thegraceyang.com/a-pure-person/); [here's another](https://www.ankitasatija.com/let-s-dutch).)
    - Always include tech stack, a link to the Git repository, a video demo, and a link to the fully deployed app/project where applicable.
    - The number of projects you include can vary; more important is QUALITY and RANGE. Showcase projects that emphasize the full range of your abilities. For more on this, [check out this article](https://levelup.gitconnected.com/the-5-must-haves-for-a-developer-portfolio-website-d0bd35ec0e89).
- **Contact Info**: Link the social media accounts that you use for professional purposes, including GitHub, Twitter, LinkedIn, Tumblr, Instagram, etc. Be sure you’re conveying a consistent image of yourself across all your social media channels that flow alongside your website’s content. This way, visitors will access the ongoing flow of your thoughts and experiences within tech. Make it quick and easy for visitors to contact and engage with you. Include your email address, embed your email address, or consider coding in a contact form, through which visitors can directly email you through your site.
- **Blog**: a personal recommendation is to be writing blog posts about your technical education through Re:Coded and beyond! Create a blog section to host these writing directly on your portfolio, which will only increase traffic and views.
- Once your site is up and running, **share it with your friends and colleagues**, link to it on your LinkedIn, social profiles, and include it in your email signature. By doing this you are continuing to build and market your brand while making it easily searchable and accessible on the web.
- **Connect your site to [Google Analytics**](http://analytics.google.com/) — then, paste the analytics tracking code into the `<head>` of the website.
    - Add these meta tags to the `<head>` of your site. For example:

        ```css
        <title>NAME</title> 
        <meta charset="utf-8" /> 
        <meta name=”description” content="Full-Stack Developer and Digital Product Manager, based in Shanghai, China"> 
        <meta name=”keywords” content="NAME,developer,Ruby,RoR,HTML,JavaScript"> 
        <meta name="author" content="NAME">
        ```

Examples / Resources: 

[20 Developer Portfolios for Inspiration 🤩](https://dev.to/jatinrao/20-developer-portfolios-for-inspiration-2k06)

[An Honest Guide to Build a Decent and Powerful Developer Portfolio](https://betterprogramming.pub/an-honest-guide-to-build-a-decent-and-powerful-developer-portfolio-2319f2cc2c19)

[https://toggl.com/blog/web-developer-portfolio](https://toggl.com/blog/web-developer-portfolio)
