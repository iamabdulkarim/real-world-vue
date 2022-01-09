<template>
<router-link class="event-link" :to="{name:'event-show', params:{id:'1'} }">
  <div class="event-card -shadow">
    <span class="eyebrow">@{{ last.time}} on {{last.date}}</span>
    <h4 class="title">{{ last.title }}</h4>
    <BaseIcon name="users">{{ last.attendees.length}} attending</BaseIcon>
     
  </div>
  </router-link> 
</template>

<script>
import BaseIcon from "./BaseIcon.vue"
  export default {
    data() {
        return {
            last: {
                id: 1,
                title: "Park Cleanup",
                date: "Tues Aug 19, 2018",
                time: "6.00",
                attendees: [
                    { id: "abc123", name: "Abu Bakkar" },
                    { id: "def456", name: "Abdul Karim" }
                ]
            }
        };
    },
    components: { BaseIcon }
}
</script>

<style  scoped>
  .event-card {
  padding: 20px;
  margin-bottom: 24px;
  transition: all 0.2s linear;
  cursor: pointer;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2), 0 1px 15px 0 rgba(0, 0, 0, 0.19);
}
.event-card > .title {
  margin: 0;
}
.event-link {
  color: black;
  text-decoration: none;
  font-weight: 100;
}
</style>