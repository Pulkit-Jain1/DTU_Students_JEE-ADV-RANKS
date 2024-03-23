# DTU_Students_JEE-ADV-RANKS
# DTU_JEE_Adv_Ranks

Jee(Advance) Rank Checker for DTU Students(Batch 2022 and Batch 2023)[DATA ANALYSIS PROJECT]-

**How it works?**

* Let's explore how this operates by using the example of the 2022 batch:
* 
* We are aware that DTU publicly releases the mapping of roll numbers, names, and application numbers for each student on their website. The application number mentioned in the PDF corresponds to the Main's roll number.

* For the 2022 batch specifically, students' roll numbers are changed in the second year, with their branch information attached. DTU releases a mapping of old roll numbers to new roll numbers for this purpose. Therefore, we can utilize these two PDFs to obtain the student's name, their DTU second-year roll number, and their Mains application number.

* While it may seem intuitive to use Excel for this purpose, the challenge lies in its slow processing speed and the fact that the PDFs provided by DTU are not well-structured for direct conversion to Excel. However, despite these limitations, Excel can still be used for data manipulation and cleaning, albeit requiring additional effort. In my case, I opted to utilize Python libraries, as detailed later on, to overcome these challenges and streamline the process.
Now that we have obtained the Mains application number of each student, the next step would be to...

* JEE(ADV) releases reports annually containing mappings of JEE Mains application numbers to JEE(ADV) roll numbers. However, the datasets consist of nearly 3.5 lakh students, and within the JEE(ADV) report, there is also mapping of each roll number to their Common Rank List (CRL) and category rank, resulting in a total dataset of well above 5 lakhs. Given the large dataset, the only viable option is to utilize Python libraries for data analysis and to write highly optimized code with algorithms that have excellent time complexity. By optimizing my algorithm to the highest possible degree, it took approximately 5 minutes with throttling for my 12700h to run initial extraction part, and the temperature rose to 95 degrees Celsius. Additionally, I had to run the algorithm multiple times as further code depended on it. Numerous edge cases emerged, such as handling category rank data, which I did not take into account, as I focused solely on CRL, EWS, OBC, SC, and ST categories.

* Finally, I had to convert the data to Excel for data cleaning. There were some unexpected behaviors of Python due to the unprofessional code I wrote. As a result, I needed to clean up the data and ultimately converted it to JSON format.

* I have provided the Python code that I used along with the HTML, CSS, and JS files. It was recommended to develop a backend for this website as it contains student data. However, the data is already public, and furthermore, I neither had the time nor the knowledge to implement it. Moreover, I didn't want to spend money in dollars for hosting this simple website. I extensively used ChatGPT 3.5/Gemini to help me build this project. Additionally, this is my first project, which is why I haven't followed recommended practices, making some parts of it very hard to understand.

* The UI/UX part of the website may not look good as I am not proficient in design, and the project is more focused on data analysis and extraction rather than web development.

**Can we do similar thing for Mains Rank ?**

* As of now, accessing this information isn't feasible because it necessitates the candidate's date of birth to log in from the mains website. Unlike JEE(Adv), there isn't any publicly available data. Additionally, there's captcha verification, which can be bypassed using tools like Tesseract. However, since this data isn't public, building anything upon it could potentially alert authorities to take action.

**Imporatant clarification regarding code part**

* I have converted the JSON data to JavaScript objects, which may seem unprofessional, but given the constraints of not being able to use a backend, it was the most viable approach for me.
* In the DATA-EXTRACTION code of Python, I intentionally avoided using loops after each extraction process to simplify testing. By specifying each case separately, it made the testing process more straightforward and manageable.
* In Visual Studio Code, you may need to adjust some settings to ensure the terminal displays all cases, as it typically shows only a specific number of list elements by default.
* JS code is minified for performance optimization.
* In my Python code, I have imported several libraries that are now redundant because I was experimenting with them. Additionally, the code that relied on these libraries is now commented out, allowing users to see alternate approaches.
* All the files (PDFs) that I used for code extraction are provided in the same folder as the Python code.


