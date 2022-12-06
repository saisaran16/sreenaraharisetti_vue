<template>
    <!--div v-if="book.published == false"-->

<div class="student">
    <ul><h1 style="color:cadetblue">{{student.name}}</h1></ul>
    <ul><h4>BannerID : {{student.bannerId}}</h4></ul>
    <ul><h4>Present Semester : {{student.currentSemester}}</h4></ul>
    <ul><h4>Grade :  {{student.totalGrade}}</h4></ul>
    <ul><h4>Graduated : {{student.isGraduated}}</h4></ul>
    </div>
</template>

<script>

export default{
    name: 'Student',
    props:{
        student: Array
    }
}
</script>

<style scoped>



h4{
    margin: 2px;
}

.student{
    background-color: #e3e6ec;
    color:rgb(60, 86, 135);
    padding: 1em;
    border:3px solid rgb(100, 146, 211);
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    width:100%;
    display:inline-block;
}
.student:hover {
 border: 5px solid yellow;
 color: rgb(53, 182, 152);
 box-shadow: 8px 8px rgb(110, 125, 197);
}

</style>