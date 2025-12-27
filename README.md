# TP 3 – Building a Product Form in Symfony

## Steps

1. **Import Bootstrap**  
   - Added Bootstrap 5 in the `base.html.twig` template to style the page.

2. **Create the Controller**  
   - Run: `php bin/console make:controller ProductController`  
   - This controller will display the product page and handle the form.

3. **Create the Form**  
   - Run: `php bin/console make:form ProductOrderType`  
   - This generates a Form Type class to build the form fields.

4. **Implement the Form Type**  
   - Add fields based on the HTML:  
     - `quantity` (IntegerType, min/max, default value)  
     - `color` (ChoiceType with options)  
     - `submit` (SubmitType with button style)  
   - Add needed attributes (`attr`) to match Bootstrap styling.

5. **Implement the Controller Logic**  
   - Use `$form->handleRequest($request)` to process the form.  
   - Check `isSubmitted()` and `isValid()` to validate submission.  
   - Add flash messages or handle the data as needed.

6. **Twig Template**  
   - Replace the static HTML form with Symfony form helpers:  
     - `form_start(form)`  
     - `form_widget()` for fields  
     - `form_end(form)`  
   - Keeps layout and styling using Bootstrap.

