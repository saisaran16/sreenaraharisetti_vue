<template>
    
     <div class="studentbox">
         
        <div v-for="student in student" :key="student.id" >
                
                <Student :student="student"/>
        </div>

        

     </div>

</template>

<script>

import Student from "./Student.vue"
export default{

    name: 'Studentbox',
    components: {
        Student
    },
    props: {
        student: Array
    }

}

</script>


<style>

.studentbox{

    padding: 40px;
    color: gray;
    grid-template-columns: 1fr 1fr 1fr;
    border:3px solid rgb(29, 70, 127);
    background-image: url("https://thumbs.dreamstime.com/b/graduation-cap-diploma-table-books-150016685.jpg");
    background-repeat: no-repeat;
    background-attachment: fixed;  
    background-size: cover;
}
</style>