# FormWizard

FormWizard is a jQuery plugin which turns a regular HTML form into a wizard with very little effort. 

The plugin supports AJAX form submission, form validation and browser back and forward buttons, all through integration with the following jQuery plugins:

* jQuery form
* jQuery validation
* BBQ plugin.

## Compatibility

This will be updated as more testing is completed

* **Firefox 3.5**
* **Chrome**

## Usage

Be sure to have the correct includes obviously.

* **jquery-1.4.2.min.js** or **jquery-1.4.4.min.js**
* **jquery.form.js**
* **jquery.validate.js**
* **bbq.js**
* **jquery-ui-1.8.5.custom.min.js**
* **jquery.form.wizard-{version}**

    $(function() {
        $("#demoForm").formwizard({
            formPluginEnabled: true,
            validationEnabled: true,
            focusFirstInput : true,
            formOptions : {
                success: function(data) {
                    $("#status").fadeTo(500,1,function(){ 
                        $(this).html("You are now registered!").fadeTo(5000, 0);
                    })
                },
                beforeSubmit: function(data){
                    $("#data").html("data sent to the server: " + $.param(data));
                },
                dataType: 'json',
						    resetForm: true
            }
        });
  		});


# Live Demo

The plugins official demo and documentation page can be found at http://thecodemine.org
