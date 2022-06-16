# Day03

Q1. For the given JSON iterate over all for loops (for, for in, for of, forEach)

Ans-

 var address=[{"city":"Latur",
  "area":"Shivaji chowk",
  "colony":"shrinagar colony"
  }];
 
  //for loop
  for(var i=0;i<address.length;i++)
  {
     //1st way of accessing
    let obj=address[i];
    console.log("City - "+obj.city);
    console.log("Area - "+obj.area);
    console.log("Colony - "+obj.colony);

    //2nd way of accessing
    console.log(address[i]);
  }

  //for-in loop
  for(var i in address)
  {
    console.log("City - "+address[i].city);
    console.log("Area - "+address[i].area);
    console.log("Colony - "+address[i].colony);
  }
 
  //for of loop
  for(const val of address)
  {
    console.log(val);
  }
 
  //for-each loop
  address.forEach((item)=>{
         console.log(item);
         
         //2nd way
         console.log("City - "+item.city);
         console.log("Area - "+item.area);
         console.log("Colony - "+item.colony);
         });

Q2. Create your own resume data in JSON format

Ans-

 var resume=[{
  "Firstname":"Anuja",
  "Lastname":"Mukkawar",
  "Education":"Graduation in Bachlore of Computer Science Engineering",
  "ProfessionalSummary":"I am working as skills developer in Aera Technology. I worked on SQL and Java."
  }];

 for(res in resume)
 {
    console.log("Here is my resume...");
    console.log("Firstname- "+resume[res].Firstname);
    console.log("Lastname- "+resume[res].Lastname);
    console.log("Education- "+resume[res].Education);
    console.log("ProfessionalSummary- "+resume[res].ProfessionalSummary);
 }

Q3. Read about the difference between window, screen and document in javascript

Ans-

window is the execution context and global object for that context's JavaScript
document contains the DOM, initialized by parsing HTML
screen describes the physical display's full screen
See W3C and Mozilla references for details about these objects. The most basic relationship among the three is that each browser tab has its own window, and a window has window.document and window.screen properties. The browser tab's window is the global context, so document and screen refer to window.document and window.screen. More details about the three objects are below-

window-

Each browser tab has its own top-level window object. Each <iframe> (and deprecated <frame>) element has its own window object too, nested within a parent window. Each of these windows gets its own separate global object. window.window always refers to window, but window.parent and window.top might refer to enclosing windows, giving access to other execution contexts. In addition to document and screen described below, window properties include

setTimeout() and setInterval() binding event handlers to a timer
location giving the current URL
history with methods back() and forward() giving the tab's mutable history
navigator describing the browser software.
 
document-
 
Each window object has a document object to be rendered. These objects get confused in part because HTML elements are added to the global object when assigned a unique id. E.g., in the HTML snippet

<body>
  <p id="holyCow"> This is the first paragraph.</p>
</body>

The paragraph element can be referenced by any of the following:

window.holyCow or window["holyCow"]
document.getElementById("holyCow")
document.querySelector("#holyCow")
document.body.firstChild
document.body.children[0]
 
screen-
 
The window object also has a screen object with properties describing the physical display:

screen properties width and height are the full screen

screen properties availWidth and availHeight omit the toolbar

The portion of a screen displaying the rendered document is the viewport in JavaScript, which is potentially confusing because we call an application's portion of the screen a window when talking about interactions with the operating system. The getBoundingClientRect() method of any document element will return an object with top, left, bottom, and right properties describing the location of the element in the viewport.
