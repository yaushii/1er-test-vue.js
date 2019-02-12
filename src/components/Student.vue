<template>
<div class="studentItem">
<p>{{ me.firstname + " " +me.lastname }}</p>
<!--<div>{{ myURL }}</div>-->
</div>
</template>

<script>
export default {
    name: "Student",
    data () {
        return{
        me: {},
        }
    },

    props:{
        myURL:String,
    },

    methods:{
        getMe: function (){
            fetch
            ("http://api-students.popschool-lens.fr" + this.myURL)
            .then(r => r.json())
            .then(r =>  {
        console.log("ok")
        this.me = r;
            })
                
           

        }
    },
    mounted(){
        this.getMe()
    }

}
</script>

<style>

.studentItem {
    margin: 10px;
    background-color: #D499B9;
    margin-left: 10em;
    margin-right: 10em;
  }
</style>