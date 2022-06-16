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
 console.log("for each loop");
 address.forEach((item)=>{
         console.log(item);
         
         //2nd way
         console.log("City - "+item.city);
         console.log("Area - "+item.area);
         console.log("Colony - "+item.colony);
         });
