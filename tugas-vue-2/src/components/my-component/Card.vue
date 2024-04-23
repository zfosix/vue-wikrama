<template>
     <div class="card-service">
          <img class="img" src="@/components/img/mc.jpeg">
          <div class="text-container">
               <h3>{{ title }}</h3>
               <p>{{ description }}</p>
               <div class="footer">
                    <img class="img2" src="@/components/img/mc.jpeg">
                    <p class="text-footer">
                         {{ name }}
                         <br>
                         <span id="date">
                              {{ date }}
                         </span>
                    </p>
               </div>
          </div>
     </div>
</template>
   
<script>
export default {
     props: ['title', 'description', 'name', 'date', 'img'],
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400&display=swap");

#date
{
     font-size: 12px;
}

.footer
{
     display: flex;
}

.text-footer
{
     margin-top: 20px;
     margin-left: 10px;
}

.img2
{
     margin-top: 20px;
     border-radius: 50%;
     width: 30px;
     height: 30px;
}


.row-service
{
     display: flex;
     font-family: "Poppins", sans-serif;
     justify-content: center;
     align-items: center;
     min-height: 90vh;
}

.card-service
{
     border: none;
     border-radius: 20px;
     box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
     display: flex;
     margin: 175px auto;
     max-width: 900px;
     box-shadow: 0 0 10px black;
}

.card-service img
{
     max-width: 45%;
     margin-right: 20px;
}

.card-service:hover
{
     transform: scale(1.15);
     transition: transform 1s;
}
</style>