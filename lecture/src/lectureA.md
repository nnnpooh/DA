---
marp: true
theme: default
author: Nirand Pisutha-Arnond
paginate: true
footer: 'Workshop Part 1: Descriptive Analysis Using Pivot Table / Pivot Chart'
math: mathjax
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;700&display=swap');
    :root {
    font-family: Kanit;
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

# Workshop Part 1

## Descriptive Analysis Using Pivot Table / Pivot Chart

---

![bg](./img/A01.png)

---

![bg](./img/A02.png)

---

![bg](./img/A03.png)

---

# กิจกรรม - A1

<div class="colwrap">
<div class="left">

- สร้างแผนภูมิต่อไปนี้

  ![height:120](./img/A11.png)
  ![height:120](./img/A12.png)
  ![height:120](./img/A13.png)

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1&end=62" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

![bg](./img/A04.png)

---

![bg](./img/A05.png)

---

![bg](./img/A06.png)

---

![bg](./img/A07.png)

---

# กิจกรรม - A2-1

<div class="colwrap">
<div class="left">

- แปลงข้อมูลเป็น Excel Table
- ตั้งชื่อ Table ว่า `Sale`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=62&end=108" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A2-2

<div class="colwrap">
<div class="left">

- สร้าง “Month” คอลัมน์
- สูตร `=TEXT([@Date],"mmmm")`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=108&end=156" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A2-3

<div class="colwrap">
<div class="left">

- สร้าง “Age Group” column
  - Youth `(<25)`
    -Young Adults `(25-34)`
    -Adults `(35-64)`
    -Seniors `(>64)`
- สูตร
  `=IFS([@[Customer Age]]<25,"Youth",[@[Customer Age]]<35,"Young Adult", [@[Customer Age]] <65,"Adults",[@[Customer Age]]>=65,"Seniors")`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=156&end=197" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# Older Version of Excel

`=IF([@[Customer Age]]<25,"Youth", IF([@[Customer Age]]<35,"Young Adult", IF([@[Customer Age]] <65,"Adults", IF([@[Customer Age]]>=65,"Seniors"))))`

---

# กิจกรรม - A2-4

<div class="colwrap">
<div class="left">

- ลองใช้ Filter และ Sorting
- Tip
  - Filter ก่อนแล้วค่อย Sort มิฉะนั้นโปรแกรมจะค้าง

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=197&end=288" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A3-1

<div class="colwrap">
<div class="left">

- สร้าง Pivot table จาก `Sale` table
- Row
  - `Country`
- Values
  - `Order Quantity` (Sum of)
- Column
  - `Product Category`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=288&end=356" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A3-2

<div class="colwrap">
<div class="left">

- Format ตัวเลขให้เป็น `Currency ($)`
- `Show Values As`
  - `% of Grand Total`
- ทดลองใช้ Filter และการ Sort

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=356&end=414" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A4-1

<div class="colwrap">
<div class="left">

- สร้าง Pivot table จาก `Sale` table
- Row
  - `Year`
  - `Month`
- Values
  - `Revenue` (Sum of)
- Column
  - `Product Category`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=414&end=494" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A4-2

<div class="colwrap">
<div class="left">

- Format ตัวเลขให้เป็น `Currency ($)`
- ทดลองใช้
  - Expand / collapse
  - Filter
  - Fort

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=494&end=587" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A5-1

<div class="colwrap">
<div class="left">

- สร้าง Pivot chart
- Bar chart
  - `Revenue` vs `Country`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=587&end=631" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A5-2

<div class="colwrap">
<div class="left">

- สร้าง Pivot chart
- Line chart
  - `Revenue` vs `Date`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=631&end=660" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A5-3

<div class="colwrap">
<div class="left">

- จัด Layout
  - `Move pivot table`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=660&end=737" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A5-4

<div class="colwrap">
<div class="left">

- ทดลอง
  - Filter
  - Expand / collapse `Date`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=737&end=835" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A6-1

<div class="colwrap">
<div class="left">

- สร้าง `Timeline`
  - Interactive filter
- Tip
  - เพิ่มเนื้อที่ด้านบนโดยการขยายแถวแรก
  - ปิด `View` -> `grid`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=835&end=941" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A6-2

<div class="colwrap">
<div class="left">

- ใช้ `Report Connect` ทำให้ Filter เชื่อมต่อกับ Pivot Table ทั้งสองอัน

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=941&end=1013" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A7-1

<div class="colwrap">
<div class="left">

- สร้าง Slicer
  - `Product category`
- ใช้ `Report Connect` ทำให้ Slicer เชื่อมต่อกับ Pivot Table ทั้งสองอัน

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1013&end=1084" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A7-2

<div class="colwrap">
<div class="left">

- สร้าง Slicer

  - `Age group`
  - `Customer gender`

- ใช้ `Report Connect` ทำให้ Slicer เชื่อมต่อกับ Pivot Table ทั้งสองอัน

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1084&end=1153" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A8

<div class="colwrap">
<div class="left">

- ในข้อมูลดิบ สร้างคอลัมน์
  - `Profit = Revenue – Cost`
  - `Margin = Profit / Revenue`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1153&end=1247" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A9-1

<div class="colwrap">
<div class="left">

- สร้าง Pivot Table จาก `Sale` Table
- Row
  - `Product category`
  - `Sub category`
- Values
  - `Order Quantity`
  - `Revenue`
  - `Profit`
  - `Margin`

</div>
  <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1247&end=1331" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# กิจกรรม - A9-2

<div class="colwrap">
<div class="left">

- Format
- `Order Quantity`
  - `Show Values As` -> `% of Grand Total`
- `Revenue`, `Profit`
  - `Number format` -> `Currency ($)`
- `Margin`
  - `Number format` -> `Percent`
  </div>
    <div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1331&end=1414" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# Margin

- สิ่งที่ควรจะเป็น
  - $\text{Margin}=\frac{\Sigma (\text{Profit}) }{\Sigma (\text{Revenue})}$
- สิ่งที่เกิดขึ้น
  - $\text{Margin}= \Sigma \Big( \frac{\text{Profit}}{\text{Revenue}} \Big)$
- แก้ไขโดยใช้ `Calculated Field`

---

# กิจกรรม - A9-3

<div class="colwrap">
  <div class="left">

- ลบคอลัมน์ `Margin` จาก Pivot Table และ Table
- Refresh ข้อมูล

  - `PivotTable Analze` -> `Refresh`

    </div>
    <div class="right inverted">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1414&end=1451" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>

---

# กิจกรรม - A10-1

<div class="colwrap">
  <div class="left">

- สร้าง Calculated Field `Profit2`
- ไปที่
  - `PivotTable Analyze` -> `Fields, Items, & Sets` -> `Calculated Field...`
- Formula

  - `Profit2 = Revenue – Cost`

    </div>
    <div class="right inverted">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1451&end=1547" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>

---

# กิจกรรม - A10-2

<div class="colwrap">
  <div class="left">

- สร้าง Calculated Field `Margin`
- Formula
  - `Margin = Profit / Revenue`
  - `Margin = Profit2 / Revenue`
- Format
  - `Percent`
    </div>
    <div class="right inverted">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1547&end=1625" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>

---

# กิจกรรม - A11

<div class="colwrap">
  <div class="left">

- ใช้ `Conditional formatting`

  - `Order Quantity`: Gradient
  - `Profit`: Color

    </div>
    <div class="right inverted">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/o9CltPjbJcc?start=1625" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>
