Simple Accordion
===================

simpleAccordion is a simple yet customizable jQuery accordion plugin which has support for nested accordion panels, custom open/close animations, easing effects and callbacks.


How to use it:
=========

1. Add the data-behavior="accordion" attribute to each accordion header and set the data-multiple to true if your accordion has nested accordion items.

<pre>
<code>
<div class="accordion-group" data-behavior="accordion">
  <p class="accordion-header default-open">
    Item 1
  </p>
  <div class="accordion-body">
    Item 1
  </div>
  <p class="accordion-header">
    Item 2
  </p>
  <div class="accordion-body">
    <div class="accordion-group" data-behavior="accordion" data-multiple="true">
      <p class="accordion-header">
        Item 2.1
      </p>
      <div class="accordion-body">
        Item 2.1
      </div>
      <p class="accordion-header">
        Item 2.2
      </p>
      <div class="accordion-body">
        Item 2.2
      </div>
    </div>
  </div>
</div>
</code>
</pre>

2. Put jQuery library and the jQuery simpleAccordion plugin's script at the bottom of the html page.
<pre>
<script src="js/jquery.min.js"></script>
<script src="js/jquery.simpleaccordion.js"></script>
</pre>
3. Initialize the plugin and done.
<pre>
$('[data-behavior=accordion]').simpleAccordion();
</pre>
4. There are a few options you can use when initializing the plugin.
<pre>
$('[data-behavior=accordion]').simpleAccordion({

  // is multiple?
  multiple: false,

  // animation speed
  speedOpen: 300,
  speedClose: 150,

  // easing effects
  easingOpen: null,
  easingClose: null,

  // CSS classes
  headClass: 'accordion-header',
  bodyClass: 'accordion-body',
  openClass: 'open',
  defaultOpenClass: 'default-open',

  // callbacks
  cbClose: null, //function (e, $this) {},
  cbOpen: null //function (e, $this) {}
  
});
</pre>
5. Apply your custom CSS styles to the accordion. Here're default CSS styles you can use them directly.
<pre>
.accordion-group { margin: 0 0 30px }

.accordion-group { margin: 0 }

.accordion-body {
  display: none;
  padding: 10px 20px 14px;
  background-color: #f6f6f6;
  border-radius: 5px;
  margin: 4px 0;
}

.accordion-body > * > .accordion-body {
  background-color: #ededed;
  margin: 0
}

.accordion-header {
  background: #e7e9ea url("../img/accordion-closed.png") no-repeat 20px center;
  margin: 8px 0;
  color: #555;
  padding: 8px 40px;
  cursor: pointer;
  border-radius: 5px;
  position: relative;
}

.accordion-header.open {
  background: #999 url("../img/accordion-opened.png") no-repeat 19px center;
  color: #fff;
  font-weight: bold
}

.accordion-header:last-of-type { margin-bottom: 0 }

.accordion-header.open:last-of-type { margin-bottom: 4px }

.accordion-header span {
  position: absolute;
  right: 6px;
  top: 6px;
  background: #fff;
  padding: 2px 5px;
  border-radius: 4px;
  color: #333;
  font-weight: normal
}
</pre>

Credits :
=========

https://github.com/tomreid76/jquery-simpleAccordion