---
marp: true
theme: default
author: Nirand Pisutha-Arnond
paginate: true
footer: 'Workshop Part B: Descriptive Analysis Using Power BI / Chart'
math: mathjax
---

<style>
    :root {
    font-family: kanit light;
}
div.colwrap {
  background-color: inherit;
  /* background-color: red; */
  color: inherit;
  width: 100%;
  height: 100%;
  position: relative;
}
/* div.colwrap div h1:first-child, div.colwrap div h2:first-child {
  margin-top: 0px !important;
} */
div.colwrap div.left {
  position: absolute;
  top: 0;
  bottom: 0;
  padding: 0px 0px 0px 0px;
}

div.colwrap div.right {
  position: absolute;
  top: 0;
  bottom: 0;
  padding: 0px 0px 0px 0px;
  /* display:flex;
  flex-direction: row;
  align-items: center; */
}

div.colwrap div.left {
/* background-color: green; */
  right: 53%;
  left: 0;
}
div.colwrap div.right {
  left: 50%;
  right: 0;
}
</style>

<!-- Slide Start -->

# Workshop

## Part 2: Descriptive Analysis Using Power BI

---

# ปัญหา

- ไม่สามารถรวม Table หลายๆ อันได้
  - ต้องใช้ `VLOOPUP` ทำให้ตารางใหญ่ขึ้นเรื่อยๆ
- ข้อจำกัดในการคำนวณ
  - % Growth ของ `Revenue`

---

# เครื่องมือ

- Power Pivot
  - Microsoft Excel 2016 ขึ้นไป
  - Microsoft 365
- Tableau
  - แพง
- Power BI Desktop
  - Free
  - PC Only

---

# Power BI vs Power BI Desktop

- Power BI
  - A business analytics service by Microsoft.
  - Provide interactive visualizations and business intelligence capabilities.
- Power BI Desktop
  - The Windows-desktop-based application for PCs and desktops,
    primarily for designing and publishing reports to the Service.

## ![bg contain right:30%](./img/B01.png)

---

# กิจกรรม - B1

<div class="colwrap">
  <div class="left">

- นำเข้าข้อมูล `Sale` จาก `Sale.xlsx`

  - `File` -> `Get data` -> `Excel workbook`
  - เลือก ไฟล์ `Sale.xlsx`
  - กด `Load`

    </div>
    <div class="right inverted">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>

---

# กิจกรรม - B2-1

<div class="colwrap">
  <div class="left">

- สร้าง คอลัมน์ `Month`

  - แทป `Table tools` -> `New column`

- สูตร

  - `Month = MONTH([date])`

    </div>
    <div class="right inverted">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>

---

# กิจกรรม - B2-2

<div class="colwrap">
  <div class="left">

- สร้าง คอลัมน์ `Age Group`
- `Age Group = SWITCH(TRUE(), [Customer Age] < 25, "Youth", AND([Customer Age] >= 25, [Customer Age]<35), "Young Adult", AND([Customer Age] >= 35, [Customer Age]<65), "Adult", [Customer Age]>=65, "Senior", BLANK() )`

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B3

<div class="colwrap">
  <div class="left">

- นำเข้าข้อมูล `Customer Demographic`
  - `File` -> `Get data` -> `Text/CSV`
  - เลือก ไฟล์ `Demo.csv`
  - `Load`

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B4-1

<div class="colwrap">
  <div class="left">

- ทดลองสร้าง Relationship ใหม่

  - ลบ `Relationship` เดิมออก
  - ลาก `Customer ID` ไปทับอีกอัน

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B4-2

<div class="colwrap">
  <div class="left">

- ลองสร้าง `Column` ใหม่ใน Sale ที่มาจาก `Demo` Table
- สูตร
  - `MartialStatus = RELATED(Demo[MaritalStatus]`
  - สามารถลบออกได้ไม่จำเป็นต้องมี

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B5-1

<div class="colwrap">
  <div class="left">

- สร้าง Line Chart
- Axis
  - `Date`
- Legend
  - `Product Category`
- Values
  - `Revenue`

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B5-2

<div class="colwrap">
  <div class="left">

- Format value ให้เป็น `Currency ($)`
- `Data` -> `Column tools`

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B5-3

<div class="colwrap">
  <div class="left">

- ทดลอง ปุ่มต่างๆใน Visual
  - `Go to the next level in the hierarchy`
  - `Expand all down one level in the hierarchy`
  - `Drill down`
  - `Show as table`

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B6-1

<div class="colwrap">
  <div class="left">

- สร้าง Stacked Bar Chart
- Axis
  - `Country`
- Legend
  - `Product Category`
- Values
  - `Revenue`

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B6-2

<div class="colwrap">
  <div class="left">

- ทดลองการ `Cross Filtering`
- ทดลอง `Drilling Down` ใน Line Chart

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B7-1

<div class="colwrap">
  <div class="left">

- เพิ่ม Slicer
- Values
  - `Date`

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B7-2

<div class="colwrap">
  <div class="left">

- เพิ่ม 3 Slicers
- Values
  - `Age Group`
  - `Customer Gender`
  - `Yearly Income`

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

---

# กิจกรรม - B8

<div class="colwrap">
  <div class="left">

- เพิ่ม Card
- Values
  - `Customer ID`

</div>
<div class="right inverted">
<iframe width="560" height="315" src="https://www.youtube.com/embed/B2mcUr62EwE?" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>
