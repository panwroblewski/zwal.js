# zwal.js
zwal.js - automatic form validation library

a working example can be found here:

https://jsfiddle.net/panwroblewski/keksrcLe/

To hook validation to a form just add a '.zwal' class to form you want to validate.

Then use html data attributes to set rules for particular fields. These can be used:

'data-zwal=""'  - used for telling the library which validation rules it should run on field. 
    use these as data rules, seperated with commas(no spaces!):
    
    'isRequired' - check if fields value is not empty
    
    'isText' - check if fields value is an alphanumeric utf-8 string
    
    'isDateValid' - checks if fields value is a valid date, formatted ad yyyy/MM/dd
    
    'isEmail' - checks if fields value is a valid email address
    
    'isPesel' - checks if fields value is a valid Pesel number
    
    'isNumber' - checks if fields value is a number
    
    'selectOneOption' - checks if option is selected in select
    
    'textAreaWithOptions' - checks if fields value
    
        -one can add addition option tags for this rule:
        
        'data-zwal-max-length="x"' - for desired textareas max length
        'data-zwal-min-length="x"' - for desired textareas min length
        
  additional data attribute, that can be added to fields:
  
    'data-zwal-error-msg="message"' - for user message to be shown on validation error, if not provided a generic message will be        computed with fileds name
