<template>
  <div class="row-service">
    <Card v-for="item in data" :title="item.title" :description="item.description" :name="item.name" :date="item.date">
    </Card>
  </div>
</template>
<script>
import Card from '@/components/my-component/Card.vue';
export default {
  components: {
    Card,
    'card-service': Card
  },
  data() {
    return {
      data: [
        {
          title: ' Michie JKT48',
          description: 'Michie Alexandra, lahir 22 April 2009 atau yang lebih akrab dipanggil Indira JKT48 adalah salah seorang anggota JKT48 generasi sepuluh. Ia debut dan diperkenalkan menjadi anggota generasi ke sepuluh bersama 11 anggota lainnya pada Sabtu, 18 Desember 2021 setelah sempat tertunda dikarenakan kondisi yang tidak memungkinan saat itu.Indira juga memiliki basis penggemar fanbase yang disebut Indiraise.',
          name: 'Michie Alexandra',
          date: '22 April 2009',
        },
      ]
    }
  }
}
</script>



