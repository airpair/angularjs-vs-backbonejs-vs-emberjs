<style>
.note {
  background-color: #eee;
  padding: 20px;
  border-left: 6px solid #CE5323;
  margin: 20px 0;
  max-width: 640px; }

.note span {
  font-weight: normal;
  color: #999; }


.tut-table {
  border-collapse: collapse;
  border-spacing: 0;
  empty-cells: show;
  border: 1px solid #cbcbcb;
  margin-bottom: 1.563rem; }

.tut-table caption {
  color: #000;
  font: italic 85%/1 arial, sans-serif;
  padding: 1em 0;
  text-align: center; }

.tut-table td,
.tut-table th {
  border-left: 1px solid #cbcbcb;
  /*  inner column border */
  border-width: 0 0 0 1px;
  font-size: inherit;
  margin: 0;
  overflow: visible;
  /*to make ths where the title is really long work*/
  padding: 0.5em 1em;
  /* cell padding */ }

.tut-table td:first-child,
.tut-table th:first-child {
  border-left-width: 0; }

.tut-table thead {
  background: #f5f2f0;
  color: #000;
  text-align: left;
  vertical-align: bottom; }

/*
striping:
   even - #fff (white)
   odd  - #f5f2f0 (light gray)
*/
.tut-table td {
  background-color: transparent; }

.tut-table-odd td {
  background-color: #f5f2f0; }

/* nth-child selector for modern browsers */
.tut-table-striped tr:nth-child(2n-1) td {
  background-color: #f5f2f0; }

/* BORDERED TABLES */
.tut-table-bordered td {
  border-bottom: 1px solid #cbcbcb; }

.tut-table-bordered tbody > tr:last-child td,
.tut-table-horizontal tbody > tr:last-child td {
  border-bottom-width: 0; }

/* HORIZONTAL BORDERED TABLES */
.tut-table-horizontal td,
.tut-table-horizontal th {
  border-width: 0 0 1px 0;
  border-bottom: 1px solid #cbcbcb; }

.tut-table-horizontal tbody > tr:last-child td {
  border-bottom-width: 0; }
</style>

## 1 Introduction

In this article we are going to compare three popular MV* frameworks for the web: AngularJS vs. Backbone vs. Ember. Choosing the right framework for your project can have a huge impact on your ability to deliver on time, and your ability to maintain your code in the future. You probably want a solid, stable and proven framework to build upon, but don't want to be limited by your choice. The web is evolving fast &mdash; new technologies arise, and old methodologies quickly become irrelevant. Under this light, we are going to go through an in-depth comparison of the three frameworks.

##2  Meet The Frameworks

All the frameworks we are going to meet today have a lot in common: they are open-sourced, released under the permissive MIT license, and try to solve the problem of creating Single Page Web Applications using the MV* design pattern. They all have the concept of views, events, data models and routing. We are going to start with some quick background and history, and then dive in to compare the three frameworks.

AngularJS was born in 2009 as a part of a larger commercial product, called GetAngular. Shortly after, Misko Hevery, one of the engineers who founded GetAngular, managed to recreate a web application that consisted of 17 thousand lines of code and took 6 months to develop in a mere 3 weeks using just GetAngular. Reducing the size of the application to just about 1,000 lines of code convinced Google to start sponsoring the project, turning it into the open-source AngularJS we know today. Amongst Angular's unique and innovative features are two-way data bindings, dependency injection, easy-to-test code and extending the HTML dialect by using directives.

Backbone.js is a lightweight MVC framework. Born in 2010, it quickly grew popular as a lean alternative to heavy, full-featured MVC frameworks such as ExtJS. This resulted in many services adopting it, including Pinterest, Flixster, AirBNB and others. 

Ember's roots go way back to 2007. Starting its life as the SproutCore MVC framework, originally developed by SproutIt and later by Apple, it was forked in 2011 by Yehuda Katz, a core contributor to the popular jQuery and Ruby on Rails projects. Notable Ember users include Yahoo!, Groupon, and ZenDesk.

##3 Community

Community is one of the most important factors to consider when choosing a framework. A large community means more questions answered, more third-party modules, more YouTube tutorials&hellip;you get the point. I have put together a table with the numbers, as of June 30, 2015. Angular is definitely the winner here, being the 6th most-starred project on GitHub and having more questions on StackOverflow than Ember and Backbone combined, as you can see below:

  <table class="tut-table tut-table-bordered">
    <thead>
      <tr>
        <th>Metric</th>
        <th>AngularJS</th>
        <th>Backbone.js</th>
        <th>Ember.js</th>
      </tr>
    </thead>
    <tbody>  
      <tr>
        <td>Stars on Github</td>
        <td>40.2k</td>
        <td>18.8k</td>
        <td>14.1k</td>
      </tr>
      <tr>
        <td>Third-Party Modules</td>
        <td>1488 <a href="//ngmodules.org">ngmodules</a></td>
        <td>256 <a href="//backplug.io/">backplugs</a></td>
        <td>1155 <a href="//emberaddons.com/">emberaddons</a></td>
      </tr>
      <tr>
        <td>StackOverflow Questions</td>
        <td>104k</td>
        <td>18.2k</td>
        <td>15.7k</td>
      </tr>
      <tr>
        <td>YouTube Results</td>
        <td>~93k</td>
        <td>~10.6k</td>
        <td>~9.1k</td>
      </tr>
      <tr>
        <td>GitHub Contributors</td>
        <td>96</td>
        <td>265</td>
        <td>501</td>
      </tr>
      <tr>
        <td>Chrome Extension Users</td>
        <td>275k</td>
        <td>15.6k</td>
        <td>66k</td>
      </tr>
      <tr>
        <td>Open Issues</td>
        <td>922</td>
        <td>13</td>
        <td>413</td>
      </tr>
      <tr>
        <td>Closed Issues</td>
        <td>5,520</td>
        <td>2,062</td>
        <td>3,350</td>
      </tr>      
    </tbody>
  </table>

All those metrics, however, merely show the current state of each framework. It is also interesting to see which framework has a faster-growing popularity. Fortunately, using Google Trends we can get an answer for that too:

<iframe scrolling="no" style="border:none;" width="640" height="330" src="//www.google.com/trends/fetchComponent?hl=en-US&q=ember.js,+angularjs,+backbone.js&cmpt=q&content=1&cid=TIMESERIES_GRAPH_0&export=5&w=640&h=330"></iframe>

##4 Framework Size

Page load times are crucial for the success of your web site. Users [do not exhibit much patience](//www.fastcompany.com/1825005/how-one-second-could-cost-amazon-16-billion-sales) when it comes to the speed of browsing &mdash; so in many cases it is desired to do everything possible to make your application load as fast as possible. There are two factors to look at when considering the impact of the framework on the loading time of your application: framework size and the time it takes the framework to bootstrap. 

Javascript assets are usually served minified and gzipped, so we are going to compare the size of the minified-gzipped versions. However, merely looking at the framework is not enough. Backbone.js, despite being the smallest (only 6.5kb), requires both Underscore.js (5kb) and jQuery (32kb) or Zepto (9.1kb), and you will probably need to add some third party plug-ins to the mix.

  <table class="tut-table tut-table-bordered">
    <thead>
      <tr>
        <th>Framework</th>
        <th>Net Size</th>
        <th>Size with required dependencies</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>AngularJS 1.2.22</td>
        <td>39.5kb</td>
        <td>39.5kb</td>
      </tr>
      <tr>
        <td>Backbone.js 1.1.2</td>
        <td>6.5kb</td>
        <td>43.5kb (jQuery + Underscore)<br />
          20.6kb (Zepto + Underscore)
        </td>
      </tr>
      <tr>
        <td>Ember.js 1.6.1</td>
        <td>90kb</td>
        <td>136.2kb (jQuery + Handlebars)</td>
      </tr>
    </tbody>
  </table>

##5 Templating

Angular and Ember include a template engine. Backbone, on the other hand, leaves it up to you to use the template engine of your choice. The best way to get a feeling of the different templating engines is a code sample, so let's dive in. We will show an example of formatting a list of items as HTML.

###5.1 AngularJS

Angular's Templating engine is simply HTML with binding expressions baked-in. Binding expressions are surrounded by double curly braces: 

<!--code lang=javascript linenums=true-->

	<ul> 
		<li ng-repeat="framework in frameworks" title="{{framework.description}}"> 			  
                      {{framework.name}} 
		</li> 
	</ul>


###5.2 Backbone.js

While Backbone can be integrated with many third-party template engines, the default choice is [Underscore templates](//underscorejs.org/#template). Since Underscore is a Backbone dependency and you already have it on your page, you can easily take advantage of its templating engine without adding any additional dependencies for your application. On the downside, the templating engine of Underscore is very basic and you usually have to throw javascript into the mix, as you can see in our example:

<!--code lang=javascript linenums=true-->
    
	<ul> 
		<% _.each(frameworks, function(framework) { %> 
			<li title="<%- framework.description %>"> 
				<%- framework.name %> 
			</li> 
		<% }); %> 
	</ul>


###5.3 Ember.js

Ember currently uses the Handlebars template engine, which is an extension to the [popular](https://github.com/mustache/mustache/wiki/Other-Mustache-implementations%20) Mustache templating engine. A new Handlebars variant, called HTMLBars is currently in the works. Handlebars does not understand DOM - all it does is a simple string transformation. HTMLBars will understand DOM, so the variable interpolation will be context aware. As HTMLBars is still not production-ready, we will show the Handlebars way of printing the framework list:

<!--code lang=javascript linenums=true-->

	<ul> 
		{{#each frameworks}} 
			<li {{bind-attr title=description}}> 
				{{name}} 
			</li> 
		{{/each}} 
	</ul>


##6 AngularJS
###6.1 The Good Parts

Angular has brought many innovative concepts to the world of web developers. Two-way data binding saves a lot of boilerplate code. Consider the following jQuery code snippet:

<!--code lang=javascript linenums=true-->

	$('#greet-form input.user-name').on('value', function() { 
		$('#greet-form div.user-name').text('Hello ' + this.val() + '!'); 
	});


Thanks to Angular's two-way-binding, you never have to write this code yourself. Rather, you just declare the bindings in your HTML template:

<!--code lang=javascript linenums=true-->

    <input ng-model="user.name" type="text" />
    Hello {{user.name}}!
   

Promises play a main role in the Angular cast. Javascript is a single-thread, event-loop based language, which implies that many operations (such as network communication) happen in an asynchronous manner. Asynchronous javascript code tends to grow quickly into a spaghetti of nested callbacks, better recognized as "Pyramid Code" or "Callback Hell."

Not only does Angular have the largest community and much more online content than the two others, it is also backed and promoted by Google. As such, the core team is constantly growing, resulting in innovation and tools that improve developer productivity: Protractor, Batarang, ngmin and Zone.js, just to name a few. In addition, the team collaborates with the community on the design decisions. For example, all the design documents for Angular 2.0 can be found [here](https://drive.google.com/drive/#folders/0B7Ovm8bUYiUDR29iSkEyMk5pVUk), and everyone can make suggestions directly to the design documents.

Angular helps you categorize your application building blocks into several types: Controllers, Directives, Factories, Filters, Services and Views (templates). Those are organized in turn into modules, which can depend one upon the other. Each type of building block has a different role. Views do the UI, Controllers work out the logic behind the UI, Services take care of communication with the backend and hold together pieces of common and related functionality, while Directives make it easy to create reusable components and extending HTML by defining new elements, attributes and behaviors.

The automatic Dirty Checking means that you don't have to access your model data with getters and setters — you can modify any property of an arbitrary scope object and angular will automatically detect the change and notify all the watchers for that property.

"Angular is written with testability in mind." This quote from the [unit-testing guide](https://drive.google.com/drive/#folders/0B7Ovm8bUYiUDR29iSkEyMk5pVUk) has a lot behind it - Angular indeed puts a lot of emphasis on separation of concerns, unit isolation and provides ready-to-use, powerful mocks for fundamental built-in services such as [$http](https://docs.angularjs.org/api/ngMock/service/$httpBackend) and [$timeout](https://docs.angularjs.org/api/ngMock/service/$timeout). 


###6.2 Pain Points

Angular is often criticized for the complexity of the Directives API. Transclusion, in particular, is a concept which confuses many developers and wrapping your head around all the concepts such as compiling function, pre/post linking functions, the different scope kinds (transclusion/isolate/child scope) and all the other configuration settings for directives takes some time to master.

The scope hierarchy in Angular uses Prototypal Inheritance, which is a new concept to grasp for people coming from Object Oriented languages such as Java and C#. Failing to understand scope inheritance causes many cases of frustrated developers (examples: [here](http://stackoverflow.com/questions/12618342/ng-model-does-not-update-controller-value), [here](http://stackoverflow.com/questions/19310129/ng-model-no-longer-updates-after-typing-into-text-input) and [here](http://stackoverflow.com/questions/19408883/angularjs-select-not-2-way-binding-to-model)).

[Angular Expressions](https://docs.angularjs.org/guide/expression) are used extensively in the View layer of Angular. This expression language is very powerful, sometimes too powerful. It lets the developer use complicated logic and even perform assignment operations and calculations, all inside the view templates. Putting logic inside the templates makes it harder to test, as it becomes impossible to test it in isolation.  Consider the following code example, which clearly shows how easily the template language can be abused: 

<!--code lang=markup linenums=true-->    
    
    <button ng-click="(oldPassword && checkComplexity(newPassword) && oldPassword != newPassword) ? (changePassword(oldPassword, newPassword) && (oldPassword=(newPassword=''))) : (errorMessage='Please input a new password matching the following requirements: ' + passwordRequirements)">Click me</button>

In many cases, mistakes such as misspelling a directive name or calling an undefined scope function are silently ignored and can be challenging to find, especially when you throw into the mix the complexity of the directive API and the scope inheritance mentioned above. I have seen developers spending hours scratching their head trying to figure out why an event binding didn't fire the callback function on the scope, only to find out they have used the camelCase convention instead of the hyphen-separated one when spelling attribute names (example [here](http://stackoverflow.com/questions/16028594/angular-scope-confusion/16028814)).

Finally, the Digest Cycle of angular, which takes care of the "Magical" dirty checking, has the tendency to surprise developers. It is easy to forget to call $digest() when running in non-Angular context ([example](http://stackoverflow.com/questions/22726790/angularjs-variable-not-updating)). On the other hand, you have to be very careful not to cause slow watches or infinite digest loops (examples: [here](http://stackoverflow.com/questions/24592283/angular-infinite-digest-loop), [here](http://stackoverflow.com/questions/23684711/infdig-infinite-digest-loop) and [here](http://stackoverflow.com/questions/21322755/tracking-down-infinite-digest-errors)). In general, for pages with a lot of interactive elements, Angular becomes really slow. A good rule of thumb is not to have more than 2,000 active bindings on the same page. 

##7 Backbone.js
###7.1 The Good Parts

Backbone is lightweight, fast and has a small memory footprint. The learning curve is very linear, and there are only a few simple concepts to grasp (Models/Collections, Views, Routes). It has great documentation, the code is simple and heavily documented, and there is even an [annotated version](http://backbonejs.org/docs/backbone.html) of the code which explains how it works in detail. You can actually go over the entire source code of the framework and get familiar with it in less than an hour.

Being so small and basic, Backbone can be a good foundation to build your own framework upon. Some examples of 3rd party frameworks based on Backbone are Aura, Backbone UI, Chaplin, Geppetto, Marionette, LayoutManager, Thorax, Vertebrae. With Angular and Ember you usually have to live with the choices made by the authors of the frameworks, which may or may not suit your project needs and personal style. Angular 2.0 promises to change it, by comprising small independent modules, so you will be able to pick and mix. We are yet to see if they will be able to deliver this.

###7.2 Pain Points

Backbone does not provide structure. It rather provides some basic tools you can use to create structure, leaving it up to the developer to decide how to structure his application, and there are also many blanks to fill. Things such as memory management have to be carefully considered. The lack of view lifecycle management makes route/state changes prone to memory leaks unless you take care of cleaning up everything yourself.

While it is true that many of the functions not provided by Backbone itself could be filled by third-party plugins, this also means that there are many choices to be made when creating an application, as many functions have several alternative plugins. For example, nested models can be provided by Backbone.DocumentModel, BackBone.NestedTypes, Backbone.Schema, Backbone-Nested, backbone-nestify, just to name a few. Deciding which one is the best for your project requires research, which in turn takes time &mdash; and one of the main purposes of framework is to save you time.

Backbone lacks support for two-way data binding, meaning you will have to write a lot of boilerplate to update the view whenever your model changes, and to update your model whenever the view changes. See the example given above, showing how two-way in Angular.js data binding reduces boilerplate.

Views in Backbone manipulate the DOM directly, making them really hard to unit-test, more fragile and less reusable. The common practice is to look up DOM elements using CSS selectors, so changing a CSS class name, adding a new element with the same class name or even wrapping some DOM tree inside another element can break your CSS selectors and render your app unusable.

##8 Ember.js
###8.1 The Good Parts
Ember.js favors Convention over Configuration. This means that instead of writing a lot of boilerplate code, Ember can automatically infer much of the configuration itself, such as automatically determining the name of the route and the controller when defining a router resource. Ember even raises the bar by automatically creating the controller for your resource if you don't define one yourself. 

Ember includes both an excellent router and an optional data layer, called ember data. Unlike the two other frameworks, which have a very minimal data layer (Backbone's Collection/Model and Angular's `$resource`), Ember comes out of the box with a fully-fledged data module which integrates really nicely with a Ruby-on-Rails backend or any other RESTful JSON API that follows a simple set of conventions. It also provides support for [setting up fixtures](http://emberjs.com/guides/models/the-fixture-adapter/) for developing against mock API and testing.

Performance has been a major goal in the design of Ember.js. Concepts such as [The Run Loop](http://emberjs.com/guides/understanding-ember/run-loop/), which ensures that updated data only causes a single DOM update even if the same piece of data was updated several times, along with [caching of computed properties](http://emberjs.com/api/classes/Ember.ComputedProperty.html), and the ability to precompile the HandleBars templates during the build time or on your server, help to keep your application load and run fast.

###8.2 Pain Points

Ember's API changed much before it stabilized. Therefore, there is a lot of outdated content and examples that no longer work, making it confusing for developers who are making their first steps in the framework. Take a look at the [Ember Data Changelog](https://github.com/emberjs/data/blob/master/TRANSITION.md), and you will see what I mean. There are so many breaking changes, and those cause many StackOverflow answers and coding tutorials to become irrelevant (example [here)](http://stackoverflow.com/a/14456916/830623).

Handlebars pollutes the DOM with many `<script>` tags which it uses as markers to [keep the templates up to date](http://emberjs.com/guides/understanding-ember/keeping-templates-up-to-date/) with your model. This will be gone with the transition to HTMLBars, but for the time being, your DOM tree will be filled up with so many `<script>` tags you will [barely be able to recognize](http://colynb.com/posts/dom-horror-with-emberjs.html) your own code. And the worst part - this can also [break your CSS styling](https://github.com/emberjs/ember.js/issues/1893) or integration with other frameworks, such as [jQuery UI's Sortable](http://stackoverflow.com/questions/11748164/ember-js-and-jquery-sortable-how-to-work-around-the-metamorph-scripts).

##9 Summary

We have seen the strengths and weaknesses of all the three frameworks. Ember's holistic approach which embraces MVC structure will make a lot of sense for developers who have a MVC programming background in Ruby, Python, Java, C# or any other Object Oriented language. Ember also brings application performance to the table,  and excels at saving you from writing boilerplate by favoring convention over configuration. 

Backbone embraces minimalism. It is small, fast and easy to learn, and provides the minimum (or in many cases, even less than the minimum) that you need to get going.

Angular's innovative approach for extending HTML will make a lot of sense for people who are web developers in soul. With a large community and Google behind it, it is here to stay and grow, and it works well both for quick prototyping projects and large-scale production applications. 

CREDITS: Many thanks to Oren Rubin, Shai Reznik and Leon Fedotov who helped with this post.

<div class="note"><span>CREDITS:</span> Many thanks to Oren Rubin, Shai Reznik and Leon Fedotov who helped with this post.</div>
