# Problem 2


## Question 2

Different ways to make an HTML element invisible in view-port:

- visibility: hidden;

- opacity: 0;

- top: -9999px;
  left: -9999px;

- height: 0px;
  width: 0px;
  overflow: hidden;

- transform: scale(0);

- opacity: 0%;
  filter: opacity(0%);

- clip-path: circle(0);

- display: none;

- text-indent: -9999em;

- transform: translate(-999px, 0);


## Question 3


```
// index.html
<p>I am a paragraph.</p>
<p class="fancy">I am so very fancy!</p>
<div>I am NOT a paragraph.</div>
<h2>
  <span class="foo">foo inside h2</span>
  <span class="bar">bar inside h2</span>
</h2>

```

```
// style.css


/* <p> elements that are not in the class .fancy */
p:not(.fancy) {
  color: green;
}

/* Elements that are not <p> elements */
body :not(p) {
  text-decoration: underline;
}

/* Elements that are not <div> and not <span> elements */
body :not(div):not(span) {
  font-weight: bold;
}

/* Elements that are not <div>s or .fancy */
/* Note that this syntax is not well supported yet. */
body :not(div, .fancy) {
  text-decoration: overline underline;
}

/* Elements inside an <h2> that aren't a <span> with a class of foo. */
/* Complex selectors such as an element with a class are not well supported yet. */
h2 :not(span.foo) {
  color: red;
}

```