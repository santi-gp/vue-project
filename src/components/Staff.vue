<template>
  <input type="text" v-model="search" placeholder="Buscar por apellido"> 
  <div class="grid headgrid">
    <div>Avatar</div>
    <div>Nombre</div>
    <div>Apelldos</div>
    <div>Correo</div>
    <div>Teléfono</div>
    <div>Departamento</div>
  </div>
  <div v-for="(employee, index) in filterList" :key="index" class="grid">
    <div>
      <img :src="employee.photoUrl" alt="employee.photoUrl" />
    </div>
    <div>{{ employee.firstName }}</div>
    <div>{{ employee.lastName }}</div>
    <div>{{ employee.email }}</div>
    <div>{{ employee.phone }}</div>
    <div>{{ employee.department }}</div>
  </div>
  <div>{{filterList.length}} Empleados</div>
</template>
<script>
export default {
  name: "Staff",
  data() {
    return {
      search:'',
      employees: [
        {
          firstName: "amelia",
          lastName: "austin",
          photoUrl: "https://randomuser.me/api/portraits/thumb/women/9.jpg",
          email: "amelia.austin@example.com",
          phone: "(651)-507-3705",
          department: "Engineering",
        },
        {
          firstName: "bobbie",
          lastName: "murphy",
          photoUrl: "https://randomuser.me/api/portraits/thumb/women/79.jpg",
          email: "bobbie.murphy@example.com",
          phone: "(925)-667-7604",
          department: "Management",
        },
        {
          firstName: "kristin",
          lastName: "terry",
          photoUrl: "https://randomuser.me/api/portraits/thumb/women/45.jpg",
          email: "kristin.terry@example.com",
          phone: "(021)-544-1184",
          department: "Sales",
        },
        {
          firstName: "brandon",
          lastName: "griffin",
          photoUrl: "https://randomuser.me/api/portraits/thumb/men/59.jpg",
          email: "brandon.griffin@example.com",
          phone: "(509)-317-9506",
          department: "Management",
        },
        {
          firstName: "tammy",
          lastName: "gibson",
          photoUrl: "https://randomuser.me/api/portraits/thumb/women/72.jpg",
          email: "tammy.gibson@example.com",
          phone: "(815)-727-0663",
          department: "Support",
        },
      ],
    };
  },
  computed:{
      filterList(){
          return this.employees.filter(
              employee => employee.lastName.includes(this.search.toLowerCase())
          )
      }
  }
};
</script>
<style scoped>
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1.75fr 1fr 1fr;
  justify-content: center;
  align-items: center;
  margin: 2%;
}
.headgrid {
  font-weight: bold;
}
</style>