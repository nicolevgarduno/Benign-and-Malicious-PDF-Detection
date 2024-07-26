# Using Machine Learning Models & Binvis.io to Create a Benign and Malicious PDF Detection Program.

This program utilizes TensorFlow, neural networks, and binvis.io to create a Python program where a user can upload a binary visualization of their PDF to check if it is malicious or benign.

Around the world millions of people are put in dangerous situations due to phishing attack. The most popular methods of detecting malicious files have been static and dynamic analysis, but with rapid development of malicious code, new techniques to analyze and detect these types of files have become more popular.

While collecting my preliminary work for this project, I came across the paper that used Binvis.io in order to test multiple file types by running them through the program and training a Self-Organizing Incremental Neural Network (SOINN), and observing results of so. Binvis, was created by developer, Aldo Cortesi. It is a C# based website that uses visual analysis to view binary files. My project specifically focuses on .PDF files, training a basic neural network on Binvis created images, then collecting sample results to share!

I gathered data from Contagio and VirusTotal, then stored them into two folders– malicious and benign. I coded a Python program to webscrape the Binvis.io website to uploaded each individual file, generate a screenshot, then save to folders found on my local desktop. 

I used TensorFlow and the Kera library to upload data, flag bathes, and create a threshold for classification. I then trained, valdidated, and tested my batches. Afterwards, I was able to create confolutional layers, passing them through a reLu function and a dense function with a sigmoid activation to create one final flat layer! Finally, I passed the model through the adam optimizer within the TensorFlow library to specify losses and generate an accuracy rate.

After splitting the data I began the fun part– training the model! I used .fit function to train the component with an epoch of 100. I also validated my data to constantly check how well the model was being trained.

I then tested 83 benign files and 89 malicious files against the model, resulting in a true positive of 14 files, true negative of 82 files, false positive of 1 files, and a false negative of 75 files. This resulted in an accuracy of about 55%, a precision of about 93%, and a recall of about 16%.

In the future, I would love to continue to improve the model in order to better detect malicious files, possibly by adding a higher epoch, or having more files to train with. Different algorithms would ahve to be implemented to keep it constant with file size.
