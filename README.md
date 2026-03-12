
# 💻 Tech Stack:
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white) ![Selenium](https://img.shields.io/badge/-selenium-%43B02A?style=for-the-badge&logo=selenium&logoColor=white) ![Confluence](https://img.shields.io/badge/confluence-%23172BF4.svg?style=for-the-badge&logo=confluence&logoColor=white) ![Trello](https://img.shields.io/badge/Trello-%23026AA7.svg?style=for-the-badge&logo=Trello&logoColor=white) ![Jira](https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)



# 🧪 Selenium Test Automation Project:

Automated UI tests for a web application written in **Java** using **Selenium WebDriver** and **TestNG**.

The project automates selected user scenarios such as product management, package editing and drag-and-drop interactions.  
The test structure follows the **Page Object Model (POM)** pattern.

---

## 🛠 Technologies

- Java  
- Selenium WebDriver  
- TestNG  
- Maven  
- Page Object Model (POM)  
- IntelliJ IDEA  
- ChromeDriver  

---

## ✨ Features

This automation suite verifies the following functionalities:

- creating a **physical product**
- editing product configuration
- enabling product **sales visibility**
- viewing product details
- adding a product to **cart**
- managing **packages**
- changing **product order inside a package**
- removing products from packages
- verifying **drag & drop functionality**
- UI verification using assertions

---

## 📂 Project Structure

```
src
 ├─ main
 │   └─ java
 │       └─ config
 │           └─ PropertiesReader.java
 │
 └─ test
     └─ java
         ├─ pages
         │   ├─ AdminBarComponent
         │   ├─ AdminMenuPage
         │   ├─ BasePage
         │   ├─ CartPage
         │   ├─ CoursesEditPage
         │   ├─ CoursesPage
         │   ├─ CoursesPopupPage
         │   ├─ DigitalProductsPage
         │   ├─ LoginPage
         │   ├─ MediaPage
         │   ├─ PackagesEditPage
         │   ├─ PackagesPage
         │   ├─ PaymentHistoryPage
         │   ├─ PhysicalProductsEditPage
         │   ├─ PhysicalProductsPage
         │   ├─ PhysicalProductsPopupPage
         │   ├─ ProductDetailsPage
         │   ├─ ReportsPage
         │   ├─ .....
         │
         └─ tests
             ├─ AdminMenuTest
             ├─ CoursesPageTest
             ├─ PackagesPageTest
             ├─ PhysicalProductsPageTest
             └─ TestBase
```

---

## 🧱 Test Architecture

The project follows the **Page Object Model (POM)** design pattern.

Each page of the application is represented by a separate class responsible for interacting with UI elements.  
This approach separates test logic from page interactions and helps keep the tests readable and maintainable.

Example:

```
AdminMenuPage      → navigation inside admin panel
PackagesPage       → package list
PackagesEditPage   → editing package contents
```

---

## 🧪 Example Automated Scenario

One of the automated tests verifies **changing the order of products inside a package**.

Steps performed by the test:

1. Open the **Packages** section in admin panel  
2. Select a package from the list  
3. Open package editing view  
4. Navigate to **Package Contents** tab  
5. Perform **drag and drop** on products  
6. Save changes  
7. Verify that product order has changed  
8. Remove a product from the package  
9. Confirm the new number of products  

Example test fragment:

```java
editPage.dragProduct(0, 1);

editPage.clickSaveButton();

boolean orderChanged = editPage.waitUntilOrderChanges(firstBefore);

Assert.assertTrue(orderChanged, "Order did not change after drag and save");
```

---

## 📚 Test Scenarios

Automated scenarios in this project include:

- creating a physical product
- enabling product visibility in the catalog
- opening product details
- adding a product to the cart
- editing package contents
- changing the order of products in a package (drag and drop)
- removing a product from a package


---

## 📝 Notes

The automated tests require access to the target application and valid user credentials.

Example executions of the tests are available in the attached recordings.

