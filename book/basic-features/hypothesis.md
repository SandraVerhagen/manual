# Making comments on the website: Hypothesis

Hypothesis is a third-party application that allows anyone to make publicly visible comments on a website (once you create a free account). This section explains how to use and install the extension.

```{admonition} Be careful of changing website URL's!
:class: warning

Annotations created using the Hypothesis feature are linked to the specific URL of a website, so keep this in mind if you move a book, or change the file name, as you could lose track of your work! Note that while changing the URL may make a page invisible, you can still find the annotations using the _View group activity_ feature.

For example, if there is no annotation visible on this page, the URL probably changed!
```

## Set up Hypothesis in your book
Add this to `_config.yml`. Need to create an account.

```
html:
  comments:
    hypothesis: true
```
## Using Hypothesis

In this case it is easier to learn by doing! Hypothesis has been enabled for this book, but only in the _draft_ version. 

````{admonition} How to View the Draft Site
:class: tip, dropdown
You can access the draft version by adding `draft/` at the end of the main book (but before the current page). For example:

```
https://teachbooks.tudelft.nl/jupyter-book-manual/draft/basic-features/hypothesis.html
```

You can find out more about the draft and publish feature on {ref}`this page <publish_students>`.
````

Once on the draft version of this page, look at the top right corner: you will see three icons, an arrow, an eye and a note-pad. Clicking on the arrow will open the extension and allow you to view the annotations. Create an account and log in if you would like to reply or make your own annotations. You can also highlight text, but this is not publicly visible, it is only for your own reference.

## Student-controller with browser extension
Note that the annotations are only visible for the page that you are currently viewing. You can see all the Annotations on a website by opening the "Public" menu at the top of the dialog pane, selecting "Public" again in the drop-down, then "View group activity." Make sure you type in the URL to search (e.g., `teachbooks.tudelft.nl/jupyter-book-manual`).

As an alternative to activating this for everyone, you can also advise your students to use the [hypothesis browser extension](https://web.hypothes.is/start/). In this way, students are not distracted by potential unnecessary public annotation and comments by fellow students and teachers.

% THIS IS ADDED TO PAGE AS ANNOTATION:
% This is an example Annotation. Note that annotations are publicly visible, but you must create an account and be logged in to reply or make your own. You can make highlights, but they are only visible to you, not everyone. You can also see all the Annotations on a website by opening the "Public" menu at the top of this dialog pane, selecting "Public" again in the drop-down, then "View group activity." Make sure you type in the URL to search (e.g., `teachbooks.tudelft.nl/jupyter-book-manual`).


```{admonition} Tips
:class: tip

- use the {ref}`remove_from_publish` feature to enable Hypothesis in the draft book only
```