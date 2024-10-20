# RuleEngine
The main objective is to develop a simple 3-tier rule engine application(Simple UI, API and Backend, Data) that determines user eligibility based on attributes like age, department, income, spend etc.The system uses Abstract Syntax Tree (AST) to represent conditional rules and allow for dynamic creation,combination, and modification of these rules.

--> Tech stack used: Spring boot, Java, Postman, MySQL, Apache Maven, VS Code, HTML, CSS, Javascript.
-->The version of Spring boot used is 3.2.10 and JDK version 21.

#Features
Rule Creation: Build conditional rules dynamically.
AST Representation: Parse rules into AST for flexibility and efficiency.
Rule Combination: Combine multiple rules into a single, optimized AST.
Rule Evaluation: Evaluate user eligibility based on attributes.
Error Handling: Handle invalid rule strings and attribute data.
Rule Modifications: Modify existing rules on the fly.

#API Design
create_rule(rule_string): Converts a rule string into a Node-based AST.
combine_rules(rules): Combines multiple rules into a single AST.
evaluate_rule(JSON_data): Evaluates the rule AST against user attributes in JSON format.

#Example Rules:
Rule 1: ((age > 30 AND department = 'Sales') OR (age < 25 AND department = 'Marketing')) AND (salary > 50000 OR experience > 5)
Rule 2: ((age > 30 AND department = 'Marketing')) AND (salary > 20000 OR experience > 5)

#Design Choices
AST for Flexibility: The Abstract Syntax Tree (AST) allows for dynamic rule creation and efficient evaluation.
Modular API Design: Each API function is designed to be modular and extendable, allowing future functionalities like combining rules or adding error handling.
Database: Storing rules as ASTs in a database allows for scalability and easy modifications.

#Setup Instructions
-Build the Project: mvn clean install
-Database Setup: Choose a database system (e.g., MySQL).Define schema for storing rules and metadata.
-Run the Application: mvn spring-boot:run
-Test the Rule Engine.
