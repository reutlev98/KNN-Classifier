
## **KNN Classifier Project**

This repository contains a K Nearest Neighbors (KNN) classifier implemented in C++. It classifies numeric data using a server-client architecture based on sockets. The KNN Classifier is designed for efficient handling of numeric CSV files, allowing users to classify data using labeled training sets. The server supports multithreaded connections, enabling multiple clients to interact simultaneously.

### **Included Dataset**
An example dataset, the **"iris"** dataset, is included in the "data" directory to facilitate easy testing of the application.

---

## **Getting Started**

To run the KNN Classifier, follow these steps to set up both the client and server programs:

1. **Compile the Code**:
   Use the following command to compile all source files via the provided Makefile:
   ```bash
   make
   ```

2. **Launch the Server**:
   Start the server application by specifying a port number. For example:
   ```bash
   ./Server.out <port_number>
   ```

3. **Start the Client**:
   Run the client program by providing the server's IP address and port number:
   ```bash
   ./Client.out <server_ip> <server_port>
   ```

After establishing a connection, a menu will appear to guide you through the KNN Classifier functionalities.

**Note:** If there are connection issues, appropriate error messages will notify you, and both client and server programs will close.

---

## **Using the Application**

Once the client program is running, you will see a menu with several options:

1. **Upload CSV Files**: 
   - Send both training and testing CSV files to the server for classification.

2. **Set KNN Parameters**: 
   - Define the parameters for the KNN algorithm, such as the value of **K** and the chosen distance metric.

3. **Classify Data**: 
   - Execute classification on the uploaded test data using the defined KNN settings.

4. **Get Classifications**: 
   - Retrieve and display the results of the classification from the server.

5. **Download Results**: 
   - Save the classified data from the server to your local machine.

6. **Exit**: 
   - Disconnect from the server and close the client program.

---

## **Key Programming Principles**

The KNN Classifier project embodies several important programming principles to enhance maintainability and functionality:

- **Object-Oriented Design**: 
   The system uses classes and inheritance to effectively model the real-world relationships and entities involved in the classification process.

- **Modular Architecture**: 
   Code is structured into distinct classes, each handling specific tasks, which promotes code reuse and simplifies maintenance.

- **Polymorphism**: 
   By utilizing virtual functions, the design allows flexible command execution.

- **Robust Error Handling**: 
   The application includes comprehensive error management for user inputs, file operations, and network communications.

---

## **Performance Optimizations**

This KNN Classifier incorporates various optimizations for improved performance:

1. **Command Design Pattern**:
   - Actions chosen by users are encapsulated as objects, allowing for modular and extendable command execution. Each command is represented by a specific class implementing a common interface, enhancing the flexibility of the system.

2. **Input Validation**:
   - A dedicated validation class ensures that user inputs meet all necessary criteria, verifying vector sizes, preventing division by zero, and ensuring non-empty inputs.

3. **Multithreading**:
   - The server is designed to handle multiple client connections concurrently, enhancing efficiency and responsiveness.

4. **Reliable Communication**:
   - TCP/IP protocol is used for client-server communication, ensuring reliable and ordered transmission of data, which is crucial for real-time interactions.

---

## **Examples**

Here’s a sample run of the program using the iris dataset:

1. **Start the Server**:
   ```bash
   ./Server.out 8080
   ```

2. **Connect the Client**:
   ```bash
   ./Client.out 127.0.0.1 8080
   ```

3. **Upload the Dataset** and proceed with classification based on user-defined parameters.

![image](https://github.com/user-attachments/assets/5a883e34-feb9-433e-bb0c-d4e7a083cd29
)  

---

## **About This Project**

This KNN Classifier was developed as part of the **Advanced Programming** at **Bar Ilan University** during the academic year **2023**. 
It was completed in collaboration with **Ye'ela Granot** (yeela8g). The project showcases the application of advanced programming techniques, including socket programming, multithreading, and algorithm optimization.
