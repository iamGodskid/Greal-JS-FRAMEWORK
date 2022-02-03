### GREALJS FRAMEWORK
# A Javascript micro Framework for building userinterface

You can use the [editor on GitHub](https://github.com/iamGodskid/Greal-JS-FRAMEWORK/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

it is structured to to have easy syntax... managability and be fast.
as it renders directly to dom

### download/installation

[Download/install grealjs](https://github.com/iamGodskid/GrealJS/archive/refs/tags/v1.5.2.zip)

## USING GREALJS

reference these scripts after in your html file

```html

<script src="path/to/Greal.js"></script>
<script src="path/to/greal.min.js"></script>
```

## USAGE

```javascript

//buildComponents method mounts template directly to body
const app = new GrealComponent();
app.buildComponents(()=>{
    return (`
<button @click="pop" g-id="btn">{{component}}</button>
    `)
});
app.hooks({
component: "click me",
btn: "button",
})
app.bindEvent("#btn", "click", {
    event: ()=>{
        document.write("LOREM IPSUM DOLOR AMIT");
    }
});
//the above method binds events to element as it prevents element from controlling other events
//you could use the Events method 

app.Events({
pop:()=>{
alert("hello world");
}
})

//you could use the mountedComponent() method to load elements to target parent element after document loads
const App = new GrealComponent();
App.mountComponent("#app", {
    template: `
<h1 id="text">Loren ipsum dolor Amit</h1>
<span></span>
    `
});

//using Events() method to handle events
const x = new GrealComponent();
x.buildComponents(()=>{
return (`
<button @click="pop">{{popper}}</button>
`)
});
x.Events({
pop: ()=>{
alert("popped");
}
})
//grealjs provides hooks to handle data states just like the react states
x.hooks({
popper: "i am a component"
})
//recent upgrade to grealjs is
//the createStylesheet method
//it gives you privillege to work with actual css in greal

x.createStyleSheet(()=>{
return(
`
button{
background: rgb(20,230,50);
color:white;
}
`
)

})


```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/iamGodskid/Greal-JS-FRAMEWORK/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
