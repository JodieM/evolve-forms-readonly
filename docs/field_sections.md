#### Field Sections

Evolve Forms provides the ability for "Field Sections" to be added to the
Lightning Record Page which are independent of the page layout. Just drag and
drop the `Dynamic Forms - Field Section` component onto the page layout:

![Field Section](images/FieldSection.gif)

Edits from all field sections and page layouts will be orchestrated together, so
the same set of edit/save/cancel buttons control the entire page.

##### Comma Separated Field API Names

To use the `Dynamic Forms - Field Section` component, enter the "Section Label"
you would like to display and the "Comma Separated Field API Names" which you
would like to render. Use the below mapping to label fields as required, read
only, or to insert additional blank spaces:

| String Format        | Description             |
| -------------------- | ----------------------- |
| Prefix with Asterisk | Mark field as required  |
| Suffix with Asterisk | Mark field as read-only |
| Sequential Commas    | Introduce blank space   |

Here are some examples:

| Comma Separated Field API Names | Image                                             |
| ------------------------------- | ------------------------------------------------- |
| HomePhone, Email, Birthdate     | ![HomePhone, Email,Birthdate](images/CSV1.png)    |
| \*HomePhone, Email\*, Birthdate | ![*HomePhone, Email*,Birthdate](images/CSV2.png)  |
| HomePhone, Email, , Birthdate   | ![HomePhone, Email, , Birthdate](images/CSV3.png) |
|                                 |                                                   |

#### Label and Help Text Overrides

Evolve Forms provides the ability to easily override the label or help text on a
given field. 

Whilst this is less useful on this read-only implementation in existing orgs, it may be helpful to display some summary data in another way in another tab.

To accomplish this, enter a JSON object with simple key-value pairs
to define the override for a particular field.

Here are some examples:

| Override                                                                                                                                                        | Image                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| **No Overrides**                                                                                                                                                | ![No Overrides](images/CSV1.png)                       |
| **Field Label Overrides**<br/>{<br/> "HomePhone" \: "Home Telephone Number",<br/> "Email": "Personal Email Address",<br/>"Birthdate": "Date of Birth"<br/>}     | ![Field Label Overrides](images/LabelOverrides.png)    |
| **Help Text Label Overrides**<br/>{<br/> "HomePhone" \: "Home Telephone Number",<br/> "Email": "Personal Email Address",<br/>"Birthdate": "Date of Birth"<br/>} | ![Field Label Overrides](images/HelpTextOverrides.png) |

**Note:** If a field doesn't have help text defined, then a label override is
also required to define a help text override.