# Backoffice

* <strong>Dossiers</strong>
  * Add processed expenses & invoices to the ongoing quarter dossier
  * Gets an overview of how much you charged and how much you spent during a quarter with plots & CSV
  * Generate a zip folder with expenses / invoices in it, to send to your accountant
  * Search an expense or an invoice processed in a quarter
* <strong>Expenses</strong>
  * Listen to a chosen adress email where you often receive expenses (as a pdf or image attachment)
  * Upload an expense manually
  * Tag an expense with default hvat & vat prices (e.g "internet" )
  * Process an expense (send to the active dossier)
  * Search an expense by different criterias (name, description, tag, date between,...)
* <strong>Invoices</strong>
  * Create an invoice with predefined parameters (Default client ) or from an existing invoice
  * Add your daily rate, the way you charge (per hour / per day) etc
  * Upload your own template using Freemarker & html
  * Pdf generation
  * Summary (total days worked this year, total charged, plots,...)
  * Process an invoice (send to the active dossier)
* <strong>Documents</strong>
  * Keep your administrative documents in one place (contracts,...)
  * Search a document based on different criterias (title, description, date between, tag)
* <strong>Curriculum</strong>
  * Keep your CV up to date (personal info, experiences, skills,...)
  * Generates your CV as a PDF using a predefined template
  * Change the template using Freemarker & html
  * Import/Export your CV to json
  * Public parts of the CV are displayed on your website, personal infos can't be accessed unless a request form is filled
  * Publish the public parts of your CV to a RDF triplestore
* <strong>Tasks</strong>
  * Create custom tasks to be triggered on a specific date or by cron expression
  * Action tasks allows you to automate backend tasks (dump database, restore a database from a previous state, backup dossiers, timesheet generation,...)
  * In app & email notification when a task is triggered
* <strong>Timesheet (to be refined)</strong>
  * Generates timesheets for a specific month or for the whole year using an action task
  * Fill your timesheet accurately (start/stop button)
  * Generates a timesheet to PDF with your digital signature
* <strong>Gallery</strong>
  * Basic Instagram like feature for your public website
  * Choose a specific date to make an image visible
* <strong>Sparql Endpoint</strong>
  * Insert / Query the pre-installed RDF triplestore using yasgui
  * All triples uploaded will be public
* <strong>Finance</strong>
  * Search over yahoo finance stocks you are interested in
  * create portfolios & add stocks to it
  * Plots
* <strong>Uploads</strong>
  * Every files generated or uploaded in your app can be searched there
* <strong>Prospects</strong>
  * Allow people to contact you thought your website without providing your email address
  * Receive an in-app notification when someone tries to contact you
* <strong>Blog</strong>
  * Create posts, upload images, code,... with a rich text editor
  * Draft are not published
* <strong>Misc / toolbox</strong>
  * Base64 Encode/Decode
  * XPath / JsonPath
  * Date manipulation
  * RDF tools, file / text conversion from an rdf format to another, shacl validation