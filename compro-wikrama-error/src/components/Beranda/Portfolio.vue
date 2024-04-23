<template>
     <div class="portofolio">
          <h3> Portofolio Kami</h3>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iure, praesentium hic. Culpa optio, quibusdam alias.
          </p>
          <div class="row-portfolio">
               <Card></Card>
          </div>
     </div>
</template>
<script>
import Card from '@/components/Portfolio/Card.vue';
export default {
     components: {
          Card
     }
}
</script>
<style scope>
.portofolio
{
     margin-top: 80px;

}

.portofolio h3
{
     margin: auto;
     font-family: "Poppins", sans-serif;
     font-weight: 900;
     font-size: 48px;
     line-height: 70px;
     color: #042181;
     margin-bottom: 15px;
     text-align: center;
}

.portofolio p
{
     font-weight: 900;
     font-size: 14px;
     line-height: 20px;
     color: #4F556A;
     max-width: 680px;
     margin: auto;
     margin-top: 14px;
     margin-bottom: 25px;
     text-align: center;
}

.portofolio p span
{
     color: gray;
}

.row-portofolio
{
     display: grid;
     grid-template-columns: repeat(3, 1fr);
     grid-gap: 10px;
}

.portfolio
{
     margin-top: 80px;
}

.portfolio h3
{
     font-weight: 900;
     font-size: 48px;
     line-height: 35px;
     color: #042181;
     margin-bottom: 30px;
     text-align: center;
}

.row-portfolio
{
     display: grid;
     grid-template-columns: repeat(3, 2fr);
     grid-gap: 10px;
}

@media screen and (max-width: 600px)
{
     .row-portfolio
     {
          display: grid;
          grid-template-columns: repeat(1, 1fr);
          grid-gap: 10px;
     }
}


@media screen and (max-width: 600px)
{
     .row-portofolio
     {
          display: grid;
          grid-template-columns: repeat(1, 1fr);
          grid-gap: 10px;
     }
}
</style>