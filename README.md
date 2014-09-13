## Angular JS Markdown Editor / Preview

This directive is a Markdown editor and separate preview element. They can therefore be used independently. 

This uses PageDown for the conversion and sanitisation of the Markdown to HTML (i.e. the Preview element).

This uses Bootstrap-Markdown (http://toopay.github.io/bootstrap-markdown/) for the editor. The preview button has been disabled, to allow live-preview. 

Currently, the pagedown and and bootstrap-markdown libraries are included, but will be replaced with Bower in a later version.

Usage is pretty trivial. It requires

- Angular JS (obviously)
- JQuery (for the editor to work)
- Pagedown (the Markdown previewer used by StackExchange, and many other sites)
- Bootstrap-Markdown
- Bootstrap 3 css (for the markdown editor to work)

### Example

See the index.html file to see a fully working example, with the required scripts in the head.

The first example turns a normal textarea, which is bound to the `mydata` angular scope variable, into a Markdown editor. The second line then binds to this editor and produces a live preview. 

    <textarea ng-model='mydata' markdownedit></textarea>
    <markdown bind-from='mydata'></markdown>

The second example show how you can just do a preview of markdown data already available. So, not Live Preview this time, but a Markdown render. It displays the rendered markdown that is stored in a scope variable called `myMD`

    <markdown bind-from='myMD'></markdown>