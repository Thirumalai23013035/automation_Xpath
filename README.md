# automation_Xpath

## code

```
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import Select
import time

driver = webdriver.Chrome()
driver.maximize_window()


driver.get("https://www.selenium.dev/selenium/web/web-form.html")

time.sleep(2)


driver.find_element(
    By.XPATH, "//input[@id='my-text-id']"
).send_keys("Thirumalai")


driver.find_element(
    By.XPATH, "//input[@name='my-password']"
).send_keys("Thiru@123")


driver.find_element(
    By.XPATH, "//textarea[@name='my-textarea']"
).send_keys("I am a Computer Science Engineering student.")


dropdown = driver.find_element(
    By.XPATH, "//select[@name='my-select']"
)

select = Select(dropdown)
select.select_by_visible_text("Two")


checkbox = driver.find_element(
    By.XPATH, "//input[@id='my-check-2']"
)

if not checkbox.is_selected():
    checkbox.click()


radio = driver.find_element(
    By.XPATH, "//input[@id='my-radio-2']"
)

if not radio.is_selected():
    radio.click()


driver.find_element(
    By.XPATH, "//button[@type='submit']"
).click()

time.sleep(10)


message = driver.find_element(
    By.XPATH, "//div[@id='message']"
)

if message.text == "Received!":
    print("Registration submitted successfully!")
else:
    print("Registration failed!")


time.sleep(20)

```

## output:


<img width="1912" height="1077" alt="Screenshot 2026-10-08 111413" src="https://github.com/user-attachments/assets/8fa46a86-650c-465e-a2ea-846e310bead5" />

<img width="1437" height="1077" alt="Screenshot 2026-10-08 111419" src="https://github.com/user-attachments/assets/69f9045e-6f6d-4590-a787-556bd92349dd" />



