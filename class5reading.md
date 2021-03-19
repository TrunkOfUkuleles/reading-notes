## thinking in react

THinking ion react means breaking things down into therir compnent parts. Match your internal arcetecture with the visual architexture to keep straight. 
Start at the outside edge and work your way inward, from the hoplder objects, into uindividual fields. 

From there you can build a working structure in react. Start with it static, without the updating functions to make sure you are on the right track. This mneans 
no state tracking yet. 

From there identify the actions and break them down into their minimal comonent. This lets you reuse they over a variety of places. For each place that will house 
information, start to break down where iformations is held.If it doesn't change much, you won't have to hold in state. 

Once ytou know the data structure, make notes of who the parent elements are, and how they are passing props and handlers. Tis is where it gets confusing. 

AFter that, set up state and data handling keeping in mind on way data flow. 
