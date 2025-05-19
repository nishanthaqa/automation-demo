# automation-demo
#  LLM-Powered TestCafe Script Generator Demo

This repository hosts a **demo web application** designed to showcase the capabilities of an **LLM-powered TestCafe script generator**, using:

-  **Mistral** (via [Ollama](https://ollama.com)) for test script generation
-  **TestCafe** for automation execution
-  A lightweight HTML/CSS/JS frontend for real-world UI interactions

---

##  Live Demo

 [Visit the demo site on GitHub Pages](https://your-username.github.io/automation-demo/)  
*(Replace `your-username` with your GitHub username)*

Use this site as the **target application** for generating TestCafe scripts automatically with natural language prompts.

---

##  Demo Features

This site includes several testable elements commonly used in web automation:

###  Login Page
- Test valid and invalid login flows
- Credentials:
  - Username: `admin`
  - Password: `password123`
- Shows error message on failure

###  Form Submission
- Inputs: Name, Email
- Dropdown: Country selection
- Confirmation message shown after submit

###  Button with Alert
- Tests alert handling with JavaScript `alert()`

###  Sample Data Table
- Useful for row counting, content verification, filtering logic

---

##  LLM-Powered TestCafe Generation

This site is used as a **sandbox application** for a system that allows you to:

1. Describe a test scenario in natural language
2. Use **Ollama + Mistral** to generate valid TestCafe code
3. Run the tests against this live demo page

Example prompt:

Expected output (from LLM):
```js
test('Valid login shows dashboard', async t => {
  await t
    .typeText('#username', 'admin')
    .typeText('#password', 'password123')
    .click('button')
    .expect(Selector('#dashboard').visible).ok();
});
