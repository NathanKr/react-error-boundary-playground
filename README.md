<h2>Motivation</h2>
Crashing component will cause an app to crash . Crushing in production will result in white screen  - not very informative in terms of UX ..... .However, crushing components protected by Error Boundaries will not crash the app and you can provide fallback UI. Error Boundaries work like try and catch but for components 

<h2>What is an Error Boundary</h2>
Error boundaries are React components that catch JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI instead of the component tree that crashed. 
Error boundaries catch errors during rendering, in lifecycle methods, and in constructors of the whole tree below them

<h2>Error Boundary limitations</h2>
Error boundaries do not catch errors for:
<ul>
<li>Event handlers (learn more)</li>
<li>Asynchronous code (e.g. setTimeout or requestAnimationFrame callbacks)</li>
<li>Server side rendering</li>
<li>Errors thrown in the error boundary itself (rather than its children)</li>
</ul>


<h2>Problem component</h2>
This component access a props property. However, missing props result in an exception.In this case React will show white screen in production. White screen is not very informative for your client ....

<h2>Become an ErrorBoundary component</h2>
A component can become an Error Boundary if it fulfill the following
<ul>
<li>It is a class component</li>
<li>It defines either (or both) of the lifecycle methods static getDerivedStateFromError() or componentDidCatch()</li>
</ul>

<h2>Using ErrorBoundary component</h2>
Here we use ErrorBoundary over App but you can use any number of ErrorBoundary components

<h2>Production setup</h2>
<ol>
<li>npm i --> install packages , done once</li>
<li>npm run build  --> build production version</li>
<li>npm run preview --> run production version</li>
</ol>