```html
<div id="app">
  {{ message }}
    <ol>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>
  </ol>
    <button v-on:click="reverseMessage">Reverse Message</button>
</div>
## cdn : 
```
```js
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!',
       todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue' },
      { text: 'Build something awesome' }
    ]
  },
  delimiters:["${", "}"],
   mounted(){
            
   this.base_url = window.location.protocol + '//' + window.location.host + '/'
   const r = document.querySelector('#decompte');
   this.getTime('{{code_start}}','{{code_end}}',r);

  },
   methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
})
```
