# HackGT8_Lobbi
The HackGT8 repo for the 3rd Party Lobbi Web Application


**Project Description**

Lobbi is a third party web application whose main goal is to improve customer service for both companies, as well as the customer, by notifying customers of their place in the call line and the wait time.

After the customer calls the business, they get a text message that includes a code that the user can enter on the Lobbi website. Our application uses the NCR Alerts and Messaging API to carry out this functionality. In the future, we are planning on expanding it to a mobile interface. The platform requests the user to input answers to two questions customized to the company. The first question asks the user about the department they wish to conduct their business with, and the second question asks them to summarize their problem in under 200 characters. The business’s FAQs are compiled into a file and analyzed in AWS Comprehend. The NLP service then outputs a set number of keywords that represent the most common questions. These keywords are then compared against the user’s answers to the questions in the Tibco Data Science Text Similarity Analyzer, and a comparison score is assigned. If the score is high, the user’s queries are similar to the FAQs and can be answered by the FAQ page, therefore their need to speak to a human representative is low. So, if the comparison score between the FAQ keywords and the user input is high, the user is put in the back of the queue, and if the score is low then they are put in the front, relative to all other scores. Along with prioritizing the queue, Lobbi also showcases an intuitive animation that tracks the user’s progress in the queue and gives them an estimate of the time remaining until they are received by a representative. The NCR Alerts and Messages API is used here as well when each marker on the progress tracker is met. For instance, an SMS alert would be sent to the customer if they made it 50% of the way through the queue. This alert system updates the customer in the case they aren’t actively looking at the progress bar through the entire wait. 

Lobbi is able to create an estimated wait time through the data they gather as the company first begins using the application. Lobbi is able to track the number of customers, the time taken for each customer to receive help, and the most frequent questions from each department, and the general traffic patterns seen for call line. Through machine learning methods, Lobbi would be able to use the database of past wait times recorded, to generate the average time it takes to get customer support. This average time would then be used to calculate the wait time of customers depending on their spot in the queue. 

In addition to improving the waiting experience for customers, Lobbi will also provide feedback to the company on how to improve their customer support through analysis on the retention rate and quality of service. Through Lobbi, customers know exactly how long it would take to contact an employee, making them less likely to exit out of the hotline. Through the improved retention of customers, companies are able to reach more customers and improve their customer service. 

** Key Points **
- Lobbi is created for businesses who want to optimize their customer service support and improve their connection with customers. 
- Utilizing Lobbi can improve a company's retention of customers on the service line. 
- Lobbi can use data collected from a company in order to estimate wait times, as well as give feedback on how to improve their customer service.

** Future Directions **
- We're exploring methods to use machine learning to assess the urgency level of each customer to effectively prioritize and order customers as they wait for a representative. 
- We are planning on including extra questions to provide additional data in order to create a more thorough process and for customers to directly interact with companies. 
- We are looking into adding more features to keep the customer engaged and provide access to the company's resources and offers. 
- Lastly, we are looking at better customizing an interface for companies to use when creating their Lobbi pages where additional features can be added as the company sees fit. 


