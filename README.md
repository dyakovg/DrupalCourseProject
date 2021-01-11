# DrupalCourseProject
My course project for drupal course. The theme of the project is "System for online chocolate shop". The system have products with fields for: From what is the product made, What is the cocoa percentage. The system have option for listing product and making order. Search is supported by name of the product.

Faculty number of student: 20069

## Technologies used
Project is based on Drupal 9. The database is MySQL. The modules that i am using are: Paragraphs, Webforms, Pathauto.

## To install
A local installation requires a working local HTTP and database server.

I am using XAMPP and MySQL.

Import the database in localhost/phpmyadmin

Enable Apache and MySQL in the Control panel of XAMPP.

Go to xampp/htcdocs folder.

Clone the project on your local device.
```
git clone git@github.com:dyakovg/DrupalCourseProject.git
cd drupal-DrupalCourseProject
```
Update vhosts file.
```
C:\xampp\apache\conf\extra\httpd-vhosts.conf
```
Add extra rows so we can use custom url to open our project.
```
<VirtualHost *:80>
 DocumentRoot "C:/xampp/htdocs/DrupalCourseProject"
 ServerName course-project.com
 <Directory "C:/xampp/htdocs/DrupalCourseProject">
 Options Indexes FollowSymLinks MultiViews
 AllowOverride all
 Order Deny,Allow
 Allow from all
 Require all granted
 </Directory>
</VirtualHost>
```
Now we can open our project in browser using course-project.com url.

## URLs

```
/product-list
```
Displaying all products that are added to the system. I have created new content type with name ('Products') which is displayed in view with name ('Product list').

```
/team
```
Displaying Employees using Paragraph types. The Paragraph type('Employee type') is inserted into Contenty type('About us').

```
/home
```
Displaying homepage. In settings i have changed the homepage with custom one with name ('Homepage'), which is actually a Content type Basic page.
