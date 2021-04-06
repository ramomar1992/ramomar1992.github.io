# SENDING FORM DATA

When we build a form, we have to consider some kind of data validation on the client-side before we send it to the server. This form of validation is important as the first layer of security. When the user submits the form, the data will be sent to the server to perform the action the form is supposed to perform. There are several methods forms can work to act upon.

* GET: to retrieve data from the source
* POST: to send and create new data to the source
* DELETE: to delete existing data from the source
* PUT: to update data on the source

These methods are fundamental to the internet because they determine the form of the HTTP interaction between the server and the client.

## Client/Server architecture

On the client-side, the form purpose is specified on the method attribute of the form HTML markup. If we choose a different method than the actual one intended, it will cause different kinds of issues. The client, a web browser or a proxy, sends the data to the server when the form is submitted. The form's data is being checked and validated by the server and processed to achieve the desired behavior. The server then responds back with data sent to the user, tells them whether the request was processed successfully or not, or sends the data they want.

## The form element

The form element is the HTML element, where we will be putting our input fields to the user to enter the information or the data they want. There are several attributes that the form should take to determine its behavior.

### Method

The method is the action or the behavior we want from the form to achieve when the form is submitted. The most common methods used are the POST and the GET methods. 

### Action

This attribute takes a path or a URL to where the request should go to perform the method. In most cases, it would refer to a relative path on the same website. Sometimes it will refer to an absolute URL, which means that the response will come from a different sub-domain or a completely different domain. 

### Enctype

Enctype determine the type of data that is inputted in the form. It is important to set this attribute to a non-default value if we include input fields that take data other than text or data. The value should be set to `multipart/form-data` if we want to include the input type `file` in the form to enable the user to enter a file form data.

## Security concerns

Forms are the most common type of cyberattacks. Therefore we should work with them very carefully. We have to not trust the user even if they are trustworthy because other attackers might highjack this user. 

Some steps we might take other than client-side validation to decrease the chance that the form will be a source of harm to our website:

1. Escape potentially dangerous characters
2. Limit the incoming amount of data to allow only what's necessary
3. Sandbox uploaded files

These steps could prevent a huge amount of security hacks. However, only making these steps is not enough to have our website completely secured. It's always a good idea to get a security review performed by a competent third party. Don't assume that you've seen all the possible problems.
