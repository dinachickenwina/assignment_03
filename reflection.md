# Reflection

## Instructions

Reflections are a metcognitive activity where you are encouraged to think about your own thinking. It helps you build a strong understanding of your own learning. A good learner not only "knows what they know", but they "know what they don't know", too. Learning to reflect takes practice, but if your goal is to become a self-directed learner where you can teach yourself things, reflection is imperative.

- Now that you've completed the assignment, think about what you did and share your thoughts. What did you learn? What confuses you? Where did you struggle? Where might you need more practice?
- A good reflection is: **specific as possible**,  **uses the terminology of the problem domain** (what was learned in class / through readings), and **is actionable** (you can pursue next steps, or be aided in the pursuit). That last part is what will make you a self-directed learner.
- Flex your recall muscles. You might have to review class notes / assigned readings to write your reflection and get the terminology correct.
- Your reflection is for **you**. Yes I make you write them and I read them, but you are merely practicing to become a better self-directed learner. If you read your reflection 1 week later, does what you wrote advance your learning?

Examples:

- **Poor Reflection:**  "I don't understand loops."   
**Better Reflection:** "I don't undersand how the while loop exits."   
**Best Reflection:** "I struggle writing the proper exit conditions on a while loop." It's actionable: You can practice this, google it, ask Chat GPT to explain it, etc. 
-  **Poor Reflection** "I learned loops."   
**Better Reflection** "I learned how to write while loops and their difference from for loops."   
**Best Reflection** "I learned when to use while vs for loops. While loops are for sentiel-controlled values (waiting for a condition to occur), vs for loops are for iterating over collections of fixed values."

`--- Write your reflection in the file code/reflection.txt ---`
The most important concept I learned in this assignment was understanding that Streamlit reruns the entire script from the top every time the user clicks or types something. This changed how I think about keeping track of information in web apps. At first, I struggled with Part 3 because I tried to keep a counter variable at the top of the script, but it would reset to zero every time the page reran. Once I moved the counter into st.session_state and used if "files_processed" not in st.session_state to set it up only once, the problem went away. The second big trap was that the file uploader keeps its value after every rerun, so if I processed a file whenever one was uploaded, it would count the same file over and over. I fixed this by putting the processing behind a button that only returns True on the exact moment it gets clicked. Working through Parts 1 and 2 taught me how to use st.text_input, st.file_uploader, and output widgets like st.info and st.success. I also learned how to convert uploaded files from bytes to text using .getvalue().decode("utf-8") and then splitting on line breaks. What still feels tricky to me is getting the timing right for when to read from st.session_state and when to update it. I need more practice with complicated workflows to feel confident I am updating state at the right time. My next step is to look at the class examples like 2-counter-session.py to better understand when to initialize, update, and display values in relation to what the user does.