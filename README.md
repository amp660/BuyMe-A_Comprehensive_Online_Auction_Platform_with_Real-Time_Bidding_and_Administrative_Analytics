BuyMe - Online Auction System
Description
In this project, we have designed and implemented a relational database system to support the operations of an online auction system similar to eBay. We have used HTML for the user interface, MySQL for the database server, and Java, Javascript, and JDBC for connectivity between the user interface and database server.
Needed Tools and Installation

JRE, IDE (JAVA, Eclipse for EE developers)
MySQL
Apache Tomcat (install it locally in your computer for development purposes)
JDBC

Installation Steps

Install MySQL Server 8.0.21 or above on your personal computer

Download MySQL Installer from https://dev.mysql.com/downloads/mysql/
Launch MySQL workbench to establish a connection to your local MySQL server


Import schema BuyMe in your DB instance

Use the provided script "BuyMe.sql"
Open the script and run it in your MySqlWorkbench (File → Open SQL script)


Download Eclipse IDE for Java EE Developers

Visit https://eclipse.org/downloads/eclipse-packages/


Open Eclipse and import the template project (cs527)

File → Import → General → Existing Projects


Set your Tomcat server in Eclipse

If you don't have Tomcat yet:

Download from: https://tomcat.apache.org/download-80.cgi (binary distribution for your OS)
In Eclipse: Windows → Preference → Server → Runtime Environment → Add → Apache Tomcat v8.0
Or: Eclipse → Preferences → Server → Runtime Environments → Add → Apache Tomcat v8.0




Connect to your own DB instance in Project

Replace the database information with your own in ApplicationDB.java file:

Database address
Username
Password




Run the project based on Tomcat 8

Right click on the project → Run as → Run on Server → Apache → Tomcat8
Your project home page (login.jsp) will now be visible



Features of the Project
User Management

Create accounts for users
Login and logout functionality

I. Auctions

Sellers can post items for sale and create auctions
Buyers can set new bids or start automatic bidding with secret upper limits
Alerts for other buyers when higher bids are placed (manual)
Alerts for buyers when someone bids more than their upper limit (automatic)
End-of-auction process:

When closing time arrives, system checks if seller has set a reserve:

If yes and reserve is higher than last bid: no winner
If no: highest bidder wins


Winner receives alert notification



II. Browsing and Advanced Search

Browse items and view current bidding status
Search items by various criteria
User capabilities:

View bid history for any specific auction
View list of all auctions a specific buyer or seller has participated in
View list of similar items auctioned in preceding months


Alert system for users interested in specific items when they become available

III. Admin and Customer Rep Functions

Admin Functions:

Create accounts for customer representatives
Generate sales reports:

Total earnings
Earnings per item, item type, end-user
Best-selling items
Best buyers




Customer Representative Functions:

Respond to user questions (customer service)
Remove auctions or bids