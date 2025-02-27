# Buto-Plugin-WfBootstrapjs

<ul>
<li>Create modals with Javascript. Works for Bootstrap 4 and 5.</li>
<li>Create alert.</li>
<li>Create confirm.</li>
</ul>

<a name="key_0"></a>

## Widgets



<a name="key_0_0"></a>

### include

<ul>
<li>Include javascript.</li>
<li>Run i18n.</li>
<li>Add style (IE fix).</li>
</ul>
<p>Include in head.</p>
<pre><code>type: widget
data:
  plugin: wf/bootstrapjs
  method: include</code></pre>
<p>Javascript alert method is replaced by PluginWfBootstrapjs.alert.</p>

<a name="key_0_1"></a>

### Backdrop

<p>Backdrop can be set for all modals.</p>
<pre><code>PluginWfBootstrapjs.backdrop = false</code></pre>

<a name="key_1"></a>

## Methods



<a name="key_1_0"></a>

### get_i18n

<p>Translations.</p>

<a name="key_2"></a>

## Usage



<a name="key_2_0"></a>

### Modal

<p>Open modal.</p>
<pre><code>PluginWfBootstrapjs.modal({id: 'my_modal', label: 'My modal', url: '/some/url'});</code></pre>

<a name="key_2_0_0"></a>

#### id

<pre><code>id: 'my_modal'</code></pre>

<a name="key_2_0_1"></a>

#### label

<pre><code>label: 'My modal'</code></pre>

<a name="key_2_0_2"></a>

#### url

<pre><code>url: '/some/url'</code></pre>

<a name="key_2_0_3"></a>

#### size

<p>Values sm, lg, xl.</p>
<pre><code>size: 'sm'</code></pre>

<a name="key_2_0_4"></a>

#### fade

<p>Set to false to avoid animation.
Could be used if script in modal is supposed to close the modal.</p>
<pre><code>fade: false</code></pre>

<a name="key_2_0_5"></a>

#### btn_reload

<pre><code>btn_reload: true</code></pre>

<a name="key_2_0_6"></a>

#### content

<pre><code>content: 'Some content...'</code></pre>

<a name="key_2_0_7"></a>

#### Body

<p>Add content to body element.</p>
<pre><code>document.getElementById('my_modal_body').innerHTML='Add some content!';</code></pre>

<a name="key_2_0_8"></a>

#### Dom

<p>Add content to body using PluginWfDom.</p>
<pre><code>PluginWfDom.render([{type: 'div', innerHTML: [{type: 'strong', innerHTML: 'Date'}, {type: 'div', innerHTML: '2001-01-01'}]}], 'my_modal_body');</code></pre>

<a name="key_2_0_9"></a>

#### backdrop

<p>Set backdrop to false (default true) to be able to close modal when click besides.</p>
<pre><code>backdrop: true</code></pre>

<a name="key_2_0_10"></a>

#### body_bg

<p>Set body background using Bootstrap bg-(name) (optional).</p>
<pre><code>body_bg: 'light'</code></pre>

<a name="key_2_0_11"></a>

#### Jquery

<p>Hide all modals.</p>
<pre><code>$('.modal').modal('hide');</code></pre>
<p>Hide one.</p>
<pre><code>$('#element_id').modal('hide');</code></pre>

<a name="key_2_1"></a>

### Alert

<pre><code>PluginWfBootstrapjs.alert('My alert text...');</code></pre>
<p>Original javascript alert method is replaced by this method on page load using widget_include.</p>

<a name="key_2_2"></a>

### Confirm

<pre><code>function delete(any_data){
  PluginWfBootstrapjs.confirm({content: 'My confirm text...', method: function(){delete_confirmed();}, data: any_data });
}
function delete_confirmed(){
  if(PluginWfBootstrapjs.confirm_data.ok){
    console.log('do something...');
  }
}</code></pre>

