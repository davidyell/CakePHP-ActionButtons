#ActionButtons Plugin
A plugin to convert the basic boring 'View', 'Edit' and 'Delete' links to something a little nicer and with better usability.  

## Requirements
The styles are based on the [Twitter Bootstrap labels](http://twitter.github.com/bootstrap/components.html#labels-badges) so you'll need to include this somewhere on your page, or you can [include the labels `.less` file](https://github.com/twitter/bootstrap/blob/master/less/labels-badges.less).

You'll need to be running [CakePHP](http://www.cakephp.org/) `v2.x`

##Installation
###Get the code 
**Submodule**  
`git submodule add git@github.com:davidyell/CakePHP-ActionButtons.git app/Plugin/ActionButtons`  

**Clone**  
`git clone git@github.com:davidyell/CakePHP-ActionButtons.git app/Plugin/ActionButtons`  

**Download**
Download an archive version from here and unzip into `app/Plugin/ActionButtons`  

###Include the helper
In your `app/Config/bootstrap.php` you'll need to load the plugin.  `CakePlugin::load('ActionButtons');` unless you are already using `CakePlugin::loadAll();` 

Next you'll need to add the helper to your helpers array in your controller.  
`public $helpers = array('ActionButtons.Actions');` 

Then you can output either buttons or icons depending on which you need.  
`echo $this->Actions->actionButtons($id);`  
where `$id` is the id of the item you want buttons for. If you want to use icons call,  
`echo $this->Actions->actionIcons($id);`
