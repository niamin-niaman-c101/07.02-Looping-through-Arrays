---
theme: apple-basic
title: Welcome to Slidev
fonts:
  # basically the text
  sans: Prompt
---

# Looping through Arrays

---
layout: center
---

# ถ้า Array คือ "ตู้ล็อกเกอร์" 🗄️ ที่มีหลายช่อง 
# for loop ก็คือ "บุรุษไปรษณีย์" 📫 ที่ได้รับมอบหมายให้เอาจดหมายไปใส่ในล็อกเกอร์ทุกช่อง

<div class="flex justify-center">
<img src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExY2FxbjNnOTJzNjUxdW1kMmc2MnI2bXo4YTR4Znlkd2FxeW9hM25qbiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/eoIqbd2HHaKSQ/giphy.gif" alt="Array Example" style="max-width: 20%; height: auto; display: block; margin: 0 auto;">
</div>

---
layout: center
---

# เขาจะเริ่มที่ช่อง 0 แล้ว 
## เดินไปช่อง 1, 2, 3... อย่างเป็นระบบจนครบทุกช่อง


<div class="flex justify-center">
<img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExcWZ0enAxcWFxaWdka3pmdnRnYXMxZTNveG83d20wY2djanpleDU5dCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/R1WSlTDjU71wk/giphy.gif" alt="Array Example" style="max-width: 50%; height: auto; display: block; margin: 0 auto;">
</div>

---
layout: center
---

# 🔄 For Loop + Array = Great !!

## วิธีที่นิยมที่สุดในการทำงานกับข้อมูลทุกตัวใน Array

<v-click>

### เพราะ "ตัวแปรนับรอบ" (i) = "หมายเลข Index" ของ Array

</v-click>

---
layout: center
---

# 🎯 หลักการทำงาน

<div class="grid grid-cols-2 gap-8">

<div>

## ตัวแปร i เริ่มที่ 0
- เดินไปทีละช่อง: 0 → 1 → 2 → 3...
- หยุดที่ `ขนาด Array - 1`

</div>

<div>

## ใช้ array_name[i]
- เข้าถึงข้อมูลในช่องปัจจุบัน
- ทำงานกับข้อมูลในช่องนั้น

</div>

</div>

---
layout: center
---
# การวนลูปเพื่อแสดงผลข้อมูลทุกตัว

````md magic-move
```c
int numbers[5] = {10, 20, 30, 40, 50};
int array_size = 5;
```

```c
int numbers[5] = {10, 20, 30, 40, 50};
int array_size = 5;

for (int i = 0; i < array_size; i++) {
```


```c
int numbers[5] = {10, 20, 30, 40, 50};
int array_size = 5;

for (int i = 0; i < array_size; i++) {
    printf("Element at index %d is %d\n", i, numbers[i]);
}
```
````

---
layout: center
---

# การวนลูปเพื่อรับค่ามาเก็บใน Array ทุกช่อง

````md magic-move
```c
float prices[3];
int array_size = 3;
```

```c
float prices[3];
int array_size = 3;

for (int i = 0; i < array_size; i++) {
```

```c
float prices[3];
int array_size = 3;

for (int i = 0; i < array_size; i++) {
    printf("Enter price for item #%d: ", i + 1);
```

```c
float prices[3];
int array_size = 3;

for (int i = 0; i < array_size; i++) {
    printf("Enter price for item #%d: ", i + 1); // ใช้ i + 1 เพื่อให้ผู้ใช้เห็นเป็น 1, 2, 3
```

```c
float prices[3];
int array_size = 3;

for (int i = 0; i < array_size; i++) {
    printf("Enter price for item #%d: ", i + 1); // ใช้ i + 1 เพื่อให้ผู้ใช้เห็นเป็น 1, 2, 3
    scanf("%f", &prices[i]);
```

```c
float prices[3];
int array_size = 3;

for (int i = 0; i < array_size; i++) {
    printf("Enter price for item #%d: ", i + 1); // ใช้ i + 1 เพื่อให้ผู้ใช้เห็นเป็น 1, 2, 3
    scanf("%f", &prices[i]); // รับค่าเก็บในช่องที่ i
}
```
````

---
layout: center
---

# การวนลูปเพื่อคำนวณหาผลรวม

````md magic-move
```c
int scores[4] = {85, 90, 78, 92};
int sum = 0;
```

```c
int scores[4] = {85, 90, 78, 92};
int sum = 0;

for (int i = 0; i < 4; i++) {
```

```c
int scores[4] = {85, 90, 78, 92};
int sum = 0;

for (int i = 0; i < 4; i++) {
    sum = sum + scores[i];
```

```c
int scores[4] = {85, 90, 78, 92};
int sum = 0;

for (int i = 0; i < 4; i++) {
    sum = sum + scores[i]; // นำค่าในช่องปัจจุบันมาบวกสะสม
}
```

```c
int scores[4] = {85, 90, 78, 92};
int sum = 0;

for (int i = 0; i < 4; i++) {
    sum = sum + scores[i]; // นำค่าในช่องปัจจุบันมาบวกสะสม
}
printf("Total score: %d\n", sum); // แสดงผล 345
```
````

---

# ตัวอย่างโจทย์ที่ 1

## หาค่าที่มากที่สุดใน Array

**โจทย์:** เขียนโปรแกรมเพื่อหา **"ค่าที่มากที่สุด"** ใน Array ของตัวเลข

---

# การแยกปัญหาย่อย - โจทย์ที่ 1

<div class="grid grid-cols-2 gap-8">

<div>

<v-clicks>

## 1. วิเคราะห์
เราต้องเดินดูตัวเลขทุกตัวใน Array แล้วคอย "จำ" ค่าที่มากที่สุดที่เคยเจอไว้

## 2. สร้างที่เก็บค่าสูงสุด
สร้างตัวแปร `int max_value;` และสมมติให้ค่าที่มากที่สุดในตอนแรกคือ "ค่าในช่องแรกสุดของ Array" `max_value = numbers[0];`

## 3. สร้าง Loop
สร้าง `for` loop ที่วิ่งตั้งแต่ **ช่องที่สอง (index 1)** ไปจนจบ Array

</v-clicks>

</div>

<div>

<v-clicks>

## 4. เปรียบเทียบใน Loop
ในแต่ละรอบ ให้ใช้ `if` เปรียบเทียบค่าในช่องปัจจุบัน `numbers[i]` กับ `max_value` ถ้าค่าปัจจุบันมากกว่า ก็ให้อัปเดต `max_value` เป็นค่าใหม่ `if (numbers[i] > max_value) { max_value = numbers[i]; }`

## 5. แสดงผล
หลัง loop ทำงานจบ `max_value` จะเก็บค่าที่สูงที่สุดไว้

</v-clicks>

</div>

</div>

---

# โค้ดตัวอย่าง - โจทย์ที่ 1

````md magic-move
```c
int numbers[5] = {10, 25, 8, 30, 15};
int max_value;
```

```c
int numbers[5] = {10, 25, 8, 30, 15};
int max_value;

max_value = numbers[0]; // เริ่มต้นด้วยค่าในช่องแรก
```

```c
int numbers[5] = {10, 25, 8, 30, 15};
int max_value;

max_value = numbers[0]; // เริ่มต้นด้วยค่าในช่องแรก

for (int i = 1; i < 5; i++) {
```

```c
int numbers[5] = {10, 25, 8, 30, 15};
int max_value;

max_value = numbers[0]; // เริ่มต้นด้วยค่าในช่องแรก

for (int i = 1; i < 5; i++) {
    if (numbers[i] > max_value) {
```

```c
int numbers[5] = {10, 25, 8, 30, 15};
int max_value;

max_value = numbers[0]; // เริ่มต้นด้วยค่าในช่องแรก

for (int i = 1; i < 5; i++) {
    if (numbers[i] > max_value) {
        max_value = numbers[i];
    }
}
```

```c
int numbers[5] = {10, 25, 8, 30, 15};
int max_value;

max_value = numbers[0]; // เริ่มต้นด้วยค่าในช่องแรก

for (int i = 1; i < 5; i++) {
    if (numbers[i] > max_value) {
        max_value = numbers[i];
    }
}

printf("Maximum value: %d\n", max_value); // แสดงผล 30
```
````

---