
# 显性等待

## WebDriverWait

from selenium.webdriver.support.ui import WebDriverWait
WebDriverWait为显型等待，配合until()和until_not()方法，就能够根据EC而进行灵活地等待了。
它主要的意思就是：程序每隔xx秒看一眼，如果条件成立了，则执行下一步，
否则继续等待，直到超过设置的最长时间，然后抛出TimeoutException。

## expected_conditions

selenium.webdriver.support.expected_conditions (一般as EC)
EC作为预期条件，经常与util()和util_not()连用。
官方文档<https://python-selenium-zh.readthedocs.io/zh_CN/latest/5.Waits/>

下面是EC的18种方法

### title_is

    判断网页title是否与预期完全一致

### title_contains

    这两个条件验证元素是否出现，传入的参数都是元组类型的locator，如(By.ID, 'kw')
    一个只要一个符合条件的元素加载出来就通过；另一个必须所有符合条件的元素都加载出来才行

### presence_of_element_located

    是否加载到dom树
    判断是否"可见"，可见还是不可见并不是以人眼为标准，而是页面层级里是否有，包括被遮罩的层级，可以理解为加载到dom树且长宽大于0。

### visibility_of_element_located

    是否加载到dom树且长宽大于0

### visibility_of

### presence_of_all_elements_located

### text_to_be_present_in_element

### text_to_be_present_in_element_value

### frame_to_be_available_and_switch_to_it

### invisibility_of_element_located

### element_to_be_clickable - 元素展示并且可用

### staleness_of

### element_to_be_selected

### element_located_to_be_selected

### element_selection_state_to_be

### element_located_selection_state_to_be

### alert_is_present



# 隐性等待