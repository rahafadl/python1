
# Python Advanced Topics: Dates, Numbers, Strings, and Functions

## **التعامل مع التواريخ والأرقام (Dates and Numbers)**

في هذه الوحدة، سنتعلم كيفية التعامل مع التواريخ والأرقام في بايثون، مع استعراض الدوال الأساسية المستخدمة في الحسابات الرياضية ومعالجة التواريخ.

### **دوال الأرقام في بايثون:**

- **إيجاد القيمة المطلقة**:  
  دالة `abs()` تُستخدم لإيجاد القيمة المطلقة للعدد:
  ```python
  print(abs(-5))  # 5

    تقريب الرقم:
    دالة round() تُستخدم لتقريب الرقم:

print(round(3.14159, 2))  # 3.14

الرفع إلى أس:
دالة pow() تُستخدم لرفع الرقم إلى الأس:

print(pow(2, 3))  # 8

إيجاد أكبر وأصغر قيمة:
دوال max() و min() تُستخدم لإيجاد أكبر وأصغر قيمة في مجموعة من الأرقام:

print(max(1, 2, 3))  # 3
print(min(1, 2, 3))  # 1

جمع مجموعة من الأرقام:
دالة sum() تُستخدم لجمع مجموعة من الأرقام:

print(sum([1, 2, 3]))  # 6

إيجاد الجذر التربيعي:
دالة sqrt() من مكتبة math تُستخدم لإيجاد الجذر التربيعي:

import math
print(math.sqrt(16))  # 4.0

باقي القسمة:
دالة % تُستخدم لإيجاد باقي القسمة:

print(10 % 3)  # 1

إيجاد رقم عشوائي:
دالة randint() من مكتبة random تُستخدم لإيجاد رقم عشوائي بين عددين:

    import random
    print(random.randint(1, 100))  # رقم عشوائي بين 1 و 100

إنشاء التاريخ والوقت في بايثون:

    إنشاء تاريخ:
    يمكننا استخدام مكتبة datetime لإنشاء تاريخ معين:

import datetime
date = datetime.date(2021, 1, 1)
print(date)  # 2021-01-01

معرفة الوقت الحالي:
دالة datetime.now() تُستخدم للحصول على الوقت الحالي:

now = datetime.datetime.now()
print(now)  # الوقت الحالي

تحويل التاريخ إلى نص:
يمكن تحويل التاريخ إلى نص باستخدام دالة strftime():

    print(now.strftime("%Y-%m-%d %H:%M:%S"))  # 2021-01-01 12:00:00

أنواع البيانات المتقدمة (Advanced Sequence Types)

في هذه الوحدة، سنتعرف على عدة طرق ودوال للتعامل مع الأنواع المتقدمة مثل String و List و Tuple في بايثون.
القوائم (Lists):

    مفهوم Indexing:
    يسمح لك الوصول إلى عناصر القائمة باستخدام الفهرس، حيث يبدأ العد من صفر:

names = ["Ali", "Sara", "Mohammed"]
print(names[0])  # Ali

مفهوم Slicing:
يستخدم للوصول إلى جزء من القائمة:

print(names[1:3])  # ['Sara', 'Mohammed']

الدالة len():
تُستخدم لإيجاد طول القائمة:

print(len(names))  # 3

الدالة count():
تُستخدم للعدّ كم مرة يظهر عنصر معين في القائمة:

print(names.count("Sara"))  # 1

المعامل in:
للتحقق مما إذا كان عنصر ما موجودًا في القائمة:

    print("Ali" in names)  # True

الـ Tuple:

    مفهوم Tuple:
    هو نوع بيانات مشابه للقائمة، لكنه ثابت (لا يمكن تغييره):

    days = ("Sunday", "Monday", "Tuesday")
    print(days[0])  # Sunday

القواميس (Dictionaries):

    مفهوم Dictionary:
    هو مجموعة من الأزواج (مفتاح: قيمة):

    person = {"name": "Ali", "age": 25}
    print(person["name"])  # Ali

التعامل مع النصوص المتقدمة (Advanced Strings)

في هذه الوحدة سنتعرف على أهم الدوال والتقنيات المستخدمة مع النصوص (Strings) في بايثون.

    البحث باستخدام find():
    تُستخدم للبحث عن نص داخل نص آخر:

text = "Hello, World!"
print(text.find("World"))  # 7

تحويل النص إلى قائمة:
باستخدام split() يمكن تحويل النص إلى قائمة من الكلمات:

text = "apple, orange, banana"
print(text.split(", "))  # ['apple', 'orange', 'banana']

التحقق من النص باستخدام startswith():
تُستخدم للتحقق مما إذا كان النص يبدأ بكلمة معينة:

print(text.startswith("Hello"))  # True

التلاعب في النصوص باستخدام replace():
تُستخدم لاستبدال جزء من النص:

text = "Hello, World!"
print(text.replace("World", "Python"))  # Hello, Python!

إزالة الفراغات باستخدام strip():
تُستخدم لإزالة الفراغات الزائدة من بداية ونهاية النص:

    text = "   Hello   "
    print(text.strip())  # Hello

الدوال المتقدمة (Advanced Functions)

في هذه الوحدة سنتعرف على كيفية التعامل مع الدوال بطرق متقدمة في بايثون.
المفاهيم الأساسية للدوال:

    Positional Arguments:
    هي المعاملات التي يتم تمريرها إلى الدالة حسب ترتيبها:

def greet(name, age):
    print(f"Hello {name}, you are {age} years old.")

greet("Ali", 25)

Keyword Arguments:
يمكننا تحديد المعاملات عن طريق أسماء المعاملات:

greet(age=25, name="Ali")

Default Parameter:
يمكن للدالة أن تحتوي على قيم افتراضية للمعاملات:

def greet(name, age=20):
    print(f"Hello {name}, you are {age} years old.")

greet("Ali")  # age takes the default value of 20

Argument Packing:
تُستخدم لتجميع المعاملات غير المعروفة في دالة:

def greet(*args):
    for arg in args:
        print(f"Hello {arg}")

greet("Ali", "Sara", "Mohammed")

Argument Unpacking:
تُستخدم لتفكيك قائمة أو قاموس إلى معالم:

    def greet(name, age):
        print(f"Hello {name}, you are {age} years old.")

    person = ("Ali", 25)
    greet(*person)

مفهوم Dictionary Packing:

يقوم بتجميع القيم في قاموس بطريقة مرنة:

def greet(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

greet(name="Ali", age=25)

مشروع حساب يوم الميلاد
الهدف:

إنشاء برنامج يقوم بحساب عمر الأشخاص بناءً على تواريخ ميلادهم المدخلة، وتحليل اليوم الذي وُلدوا فيه.
المتطلبات:

    استلام عدد لا محدود من الأسماء والأعمار.

    حساب العمر بناءً على التاريخ المدخل.

    تحديد أكبر وأصغر شخص بناءً على العمر.

    التحقق من صحة التواريخ المدخلة.

الكود:

from datetime import datetime

# دالة لحساب العمر
def calculate_age(birthdate):
    today = datetime.today()
    birthdate = datetime.strptime(birthdate, "%d-%m-%Y")
    age = today.year - birthdate.year - ((today.month, today.day) < (birthdate.month, birthdate.day))
    return age

# دالة لتحويل تاريخ الميلاد إلى يوم الأسبوع
def get_day_of_week(birthdate):
    birthdate = datetime.strptime(birthdate, "%d-%m-%Y")
    return birthdate.strftime("%A")

# دالة للتحقق من صحة التاريخ
def is_valid_date(birthdate):
    try:
        datetime.strptime(birthdate, "%d-%m-%Y")
        return True
    except ValueError:
        return False

# دالة لمعالجة المدخلات
def process_people():
    people = []
    while True:
        name = input("Enter name (or 'exit' to stop): ")
        if name == 'exit':
            break
        birthdate = input("Enter birthdate (dd-mm-yyyy): ")
        
        if not is_valid_date(birthdate):
            print(f"Invalid date for {name}")
            continue
        
        age = calculate_age(birthdate)
        day_of_week = get_day_of_week(birthdate)
        people.append({"name": name, "age": age, "birthdate": birthdate, "day": day_of_week})

    for person in people:
        print(f"{person['name']} is {person['age']} years old and was born on {person['day']}.")

    if len(people) > 1:
        oldest = min(people, key=lambda x: x['age'])
        youngest = max(people, key=lambda x: x['age'])
        print(f"The oldest person is {oldest['name']}.")
        print(f"The youngest person is {youngest['name']}.")
    else:
        print("There is no oldest or youngest person.")
