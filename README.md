# Emory BMI GSoC 2021

<img src="https://pbs.twimg.com/profile_images/535105446957182978/4PApPZ-s_400x400.png" width="150" height="150" align="left" /> Emory BMI is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open source project repositories, released with open-source licenses including BSD 3-Clause License and MIT license. Most of them can be accessed from https://github.com/Emory-HITI, https://github.com/sharmalab, and https://github.com/NISYSLAB


Emory BMI has been a successful mentoring orgnaization for [Google Summer of Code 2019](https://github.com/sharmalab/Emory-BMI-GSoC-2019) and before! We had 4 great students in 2019. We are excited and looking forward to working with another batch of students for GSoC 2021.




# Communicating with the mentors

We are using Slack as the primary medium of communication. Find and join the Emory BMI slack workspace using the link - http://bit.ly/emory-bmi.

Each idea on this page has at least one mentor assigned. Each project idea also has a relevant channel in the Slack workspace, listed below under each project idea. Make sure to join the rooms that are relevant for the projects that you are interested in. Specific discussions on each project idea happens in those channels.
 
# List of Ideas (CURRENTLY UNDER CONSTRUCTION. PLEASE CHECK AGAIN FOR MORE IDEAS AS WE CONTINUE TO ADD MORE)
Discuss the project on Slack, and once you are ready to submit your application, use the template below. You must submit your application directly using the GSoC Program Site. If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your own idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.



**[1] TensorFlow-GUI: A Graphical User Interface for Tensorflow**

**Mentors:**  Monjoy Saha (monjoy.saha -at- emory.edu)

**Overview:** This project aims to develop a graphical user interface (GUI) for any deep learning model development and visualization of outcomes based on the existing Tensorflow functions. This interface will act just like a simulator similar to MATLAB. This technique will be helpful for the beginners who don't have sufficient programming knowledge. Moreover, our proposed concept will help to maintain the quality of the work.
              
**Present Status of the work:** Preliminary work has been done and a TensorFlow-GUI has been implemented as part of GSoC 2019 project with Emory BMI organization. The GSoC 2020 student is expected to extend or utilize the work from the previous year.

There are very few organizations that are also working on the development of almost similar kind of tools. [Deep Cognition](https://deepcognition.ai/) is one of them. Though they have many limitations including the quality of the code/output and the number of users. This is not an open source software.
              
**Proposed Methodology:** We will use existing Tensorflow functions which will be converted into the blocks of layers (e.g., convolution, transpose convolution, pooling, ReLu, etc.). The parameters of each layer can be set as per the requirements of the model. Suppose in the case of convolution layer; the user can set the values of input, weight, bias, kernel dimensions, number of output channels, etc.
 
**Benefits:** The proposed GUI will be very much helpful for the beginners or who don't have sufficient knowledge of coding. This GUI will help in maintaining the quality of the work for Emory BMI researchers as well as the broader research community. The students also have the potential to submitting a pull request upstream to the Tensorflow community, if relevant.
 

**Deliverables:** 

It is expected that GSOC students will use our existing GUI code for further developments. In the last year, we have developed the main skeleton of the GUI, which can be used to create a simple CNN model using convolution, pooling, etc., operations.  

This year we are expecting something more. Hence, it is necessary to make our GUI more robust and user-friendly.  It will be a good idea if you can migrate our existing GUI into a web-based GUI. Rather than this, we feel there have lots of options to improve the existing GUI. The first part which you can look into is the input data pipeline part. We are mainly working on medical data. The data may be images (file format .svs/.dcm/.jpg/.tif/png, etc.), texts, or signals.  Hence, it is recommended to develop an input data pipeline that supports biomedical data. You can follow the flow diagram below to improve this section. 

Locate the path of datasets--> Extract the patches of required sizes ---> convert the patches into TensorFlow supported  (like tfrecords/h5/bin, etc.) single/multiple file formats for easy and fast processing of data-->feed into the model.  

In the second part, it is necessary to include all the TensorFlow operations/Ops in the node editor section to make this GUI perfect. You must have to confirm that all the Ops are working correctly. 

In the third part, you need to improve the code editor part.  Whenever you select an operation from the drag-down menu, automatically corresponding code will be generated in this section. So, when you work on the node editor part, you must have to look into the code editor part as well.

In the fourth part, you have to create a separate window where we can use already trained models for further analysis. This section will be primarily used for the interpretability purpose.  Suppose you have a trained model. Follow the flow diagram below. 

Upload trained model---> feed an input image---> get the prediction results.

The fifth part is the Tensorboard integration part. Tensorboard is already integrated into our existing GUI. In our future development, it is required to implement the visualization of feature maps and more statistical analysis options. 


**Required Skills:** Tensorflow, Python, Natsort, Pandas, NodeJS, Electron, Jquery, Jquery-ui-dist, Rimraf, Sweetalert

**Source Code:** https://github.com/sharmalab/tensorflow-gui

**Slack room:** gsoc-emory-bmi.slack.com gui-tf

***




**[2] A front-end for Niffler DICOM Framework for machine learning pipelines and processing workflows**

**Mentors:** Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu) and Ramon Correa (ramon -at- dbmi.emory.edu) 

**Overview:**  Niffler is a framework to retrieve DICOM images from PACS real-time as a DICOM stream as well as retrospectively. Niffler consists of multiple modules, for real-time extraction, on-demand retrieval, png extraction, and scanner utilization. However, Niffler is developed as a command-line based tool. In this project, we aim to develop a front-end for Niffler, specifically for its on-demand retrieval (cold-extraction), real-time extraction (meta-extraction), png-extraction modules.

**Present Status of the work:** Currently, Niffler does not have a front-end. The users are expected to log in to the server and run the Python scripts directly, after providing the configuration as json files. This limits the wide use of Niffler as a framework, as only those who have access to the server or VM instance can run their extractions or workflows on Niffler. A proper front-end can help with this shortcoming. However, security and access control measures must be taken as the framework will handle data with PHI.

**Proposed Methodology:** There are several approaches to implement a front-end to Niffler. The student must present their approach and defend it. Especially consider how the proposed approach will ensure only the authorized users can use Niffler. Currently, only those who can access the VM can access and use Niffler. When providing a front-end such access control must be implemented so that the front-end can be used in production.

**Benefits:** The proposed front-end will make Niffler accessible and usable by more users. We are now limited to running the Python code after configuring the json files. A front end can make it more user-friendly. Furthermore, this enables how the framework can be used beyond the organizational boundaries, with proper firewalls and security mechanisms in place.

**Deliverables:** A front-end environment for Niffler. This could be an integrated web application or a modular architecture. However, the existing stand-alone execution based on command-line should continue to run as now. Several aspects must be decided. For example, how the CSV files are passed for the on-demand extraction, and how the end-user will know the location of the files for the png-extraction. Students are encouraged to make relevant assumptions and state in their proposal.

Several factors such as how the CSV file to extract the images on-demand should be passed and how the outputs are shared with the users should be considered. Students are encouraged to use the existing standards, frameworks, and toolkits towards implementing the functionality, rather than developing everything from the scratch. For example, RESTful interfaces maybe developed to pass the data to and from the Niffler backend. 
 
**Required Skills:** Python (and the relevant framework of choice).

**Source Code:** https://github.com/Emory-HITI/Niffler/

**Slack room:** gsoc-emory-bmi.slack.com niffler-fe


***

**[3] A Front-end for LoopSim Framework to model workflows with closed loops**

**Mentors:** Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu) and Babak Mahmoudi (b.mahmoudi -at- emory.edu)

**Overview:** LoopSim framework aims to facilitate workflows with loops, including simple and nested loops. Such workflows deviate from the standard workflows that consist of specific start and end services. As such, existing CWL and WDL workflow composers, including those with a compact front-end such as Rabix, cannot be used as such for loops. The current workflow frameworks limit their focus to supporting directed acyclic graphs (DAGs). Furthermore, workflow definitions can be made more efficient by representing them with more generic formats such as directed hypergraphs. A directed hypergraph supports workflows containing edges that connect multiple nodes. To support complex loops efficiently, we must expand our scope to include all the directed hypergraphs. Currently, LoopSim uses yEd GraphML editor as its front end. However, yEd is not open source and not ideal for customizing as our integrated front-end. As such, a custom front-end for LoopSim will be more advantageous.

**Present Status of the work:** Currently, LoopSim utilizes yEd to visualize its workflows. The workflows drawn using yEd are stored as GraphML files. The GraphML files are then parsed with LoopSim based on BeautifulSoup to represent them as hypergraphs in Python. The proposal is to custom-build a front-end framework to replace yEd. Students are encouraged to find open-source projects that can be extended and leveraged for the front-end.

**Proposed Methodology:** LoopSim is currently under active development. We aim to have the front-end that evolves with the framework. The students are encouraged to find open-source frameworks that support drag-and-drop of the components to create workflows with loops - as depicted in LoopSim with yEd as samples. 

**Benefits:** LoopSim currently uses yEd to design its directed hypergraphs. However, yEd is not open source. As such, adopting yEd for LoopSim poses a few challenges. First, we cannot adopt the front-end to customize based on LoopSim’s requirement. Second, as it is not open-source, a complete bundling of the framework is not possible. An open-source solution also removes the potential for vendor lockin, especially if yEd is discontinued in the future. Since this is also an on-going research project, the successful student also can contribute to the research as a co-author.

**Deliverables:** A minimal drag-and-drop front-end interface to compose workflows that can be represented by a diverse set of graphs, rather than being limited to DAGs. The minimal drag-and-drop front-end must be integrated into the existing graph parser to replace the current yEd-based graph composer. While several open-source frameworks such as Apache Airavata provide such a drag-and-drop interface, they do not offer the capability to compose workflows with loops with containerized microservices. As such, a front-end to LoopSim will make it towards a complete workflow framework. 

**Required Skills:** Python or the relevant frameworks/languages of choice.

**Source Code:** https://github.com/NISYSLAB/LoopSim

**Slack room:** gsoc-emory-bmi.slack.com loopsim-fe

***

# Application Template

The students are encouraged to follow this template. However, they are not expected to strictly follow this template. They are rather advised to clearly include all the requested information in their application.

**1) Project Title:**

**2) Abstract / Project Summary**:

Summarize the project in your own words.

**3) Student Name:**

**4) Student Email and Slack username:**

**5) Potential Mentor(s):**

**6) Personal Background (Brief CV)**

**7) Project Goals / Major Contributions**

(Enter as bullets)

..
     
..
     
..

**8) Project Schedule**

Break the timeline into periods of up to 7 days

**8.1) Community Bonding Period**

**8.2) Development Phase**

**8.3) Project Completion, testing, and documentation**

**9) Planned GSoC work hours**

This year, students are expected a 18 hours a week of contribution (as opposed to 2020 and previous editions which expected a full-time commitment of 35 hours). Please indicate the work hours (including the timezone), that you hope to work on your project. 

**10) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Please indicate if you have any lectures/classes, examinations, or other personal commitments. 

**11) Skill Set**

Your relevant skill set to complete this project. Include pointers to bug fixes, demos, and previous work.

Also include pointers to the completed Code Challenge (if applicable).

