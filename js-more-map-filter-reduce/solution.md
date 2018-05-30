// PART 1

1. Use `map` to return a new array of transformers' names.

   ```js
   transformers.map((robot) => robot.name);
   ```

2. Use `filter` to return a new array of only Autobots.

   ```js
   transformers.filter((robot) => robot.team == 'Autobot')
   ```

3. Use `filter` to return a new array of transformers with only vehicle forms.

   ```js
   transformers.filter((robot) => robot.form_type == 'vehicle')
   ```

4. Use `map` to return an array of objects that have a `name` and a `photo` property. Then, loop through the new array and append an `h1` with the name and an `img` with the photo to the DOM in `index.html`. **Do not use jQuery to do this!**

   ```js
   transformers.map(function(robot){
       return {name: robot.name,
               photo: robot.photo}
   }).forEach(element => { // < woot! woot! you can chain the loop function 
       console.log(element);
       // grab the body element from the DOM
       let body = document.querySelector("body");
       // create the img and photo elements
       let name = document.createElement('h1');
       let photo = document.createElement('img');
       // add content to the elements
       name.textContent = element.name;
       photo.src = element.photo;
       // append elements to the DOM
       body.appendChild(name);
       body.appendChild(photo);
   });
   ```
// PART 2

1. Reduce the Constructicons to form Devastator!

   ```js
   const createDevastator = (arr) => {
   //  First argument is our reducer/callback function
      return arr.reduce((acc, val, idx) => {
           acc.name = 'Devastator',
           acc.team = val.team,
           acc.form[val.bodyPart] = val.name
           //  Always return the accumulator (for the next iteration)
           return acc;
      }, {form: {}}) // The 2nd argument (optional) is the initial value
   }
   createDevastator(constructicons)
   })
   ```
