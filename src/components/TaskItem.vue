<template>
  <div class="task">
    <div class="barStats"></div>
    {{ text }}
    <div class="statsOptions">
      <svg id="deleteIcon" @click="deleteTask" xmlns="http://www.w3.org/2000/svg" width="19" height="21" viewBox="0 0 19 21" fill="none">
        <path d="M12.7963 5.0559V4.32997C12.7963 3.31358 12.7963 2.80539 12.5985 2.41718C12.4245 2.0757 12.1469 1.79806 11.8054 1.62407C11.4172 1.42627 10.909 1.42627 9.89259 1.42627H8.44074C7.42435 1.42627 6.91615 1.42627 6.52794 1.62407C6.18646 1.79806 5.90883 2.0757 5.73484 2.41718C5.53704 2.80539 5.53704 3.31358 5.53704 4.32997V5.0559M7.35185 10.0466V14.5837M10.9815 10.0466V14.5837M1 5.0559H17.3333M15.5185 5.0559V15.2189C15.5185 16.7434 15.5185 17.5057 15.2218 18.0881C14.9608 18.6003 14.5444 19.0167 14.0322 19.2777C13.4498 19.5744 12.6876 19.5744 11.163 19.5744H7.17037C5.64578 19.5744 4.88349 19.5744 4.30117 19.2777C3.78896 19.0167 3.37251 18.6003 3.11152 18.0881C2.81481 17.5057 2.81481 16.7434 2.81481 15.2189V5.0559" stroke="#333333" stroke-width="1.81481" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
      <svg id="finishedIcon" xmlns="http://www.w3.org/2000/svg" width="22" height="23" viewBox="0 0 22 23" fill="none">
        <path d="M20.1853 10.6707V11.5055C20.1841 13.4623 19.5505 15.3663 18.3789 16.9335C17.2073 18.5007 15.5605 19.6472 13.684 20.202C11.8076 20.7568 9.80203 20.6902 7.96654 20.0121C6.13104 19.334 4.56393 18.0807 3.49891 16.4392C2.43389 14.7976 1.92803 12.8558 2.05678 10.9033C2.18553 8.95079 2.94198 7.0922 4.21333 5.60473C5.48467 4.11726 7.20278 3.08061 9.11143 2.64937C11.0201 2.21814 13.017 2.41544 14.8043 3.21183M20.1853 4.24108L11.1112 13.3242L8.38896 10.602" stroke="#333333" stroke-width="1.81481" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    text: String
  },
  methods: {
    deleteTask() {
      this.$emit('delete-task', this.text);
    }
  }
};
</script>

<style scoped>
.task{
 color: #C9C9C9;
 font-size: 16px;
 font-weight: 700;
 display: inline-flex; 
 background-color: #1C1C1C;
 padding: 11px 14px;
 align-items: flex-start;
 width: 480px;
 border-radius: 15px;
 align-items: center;  /*alinhados*/
}

.statsOptions {
  display: inline-flex;
  margin-left: auto;
  gap: 8px; 
}

#deleteIcon, #finishedIcon {
  cursor: pointer;
}

#deleteIcon:hover path {
    stroke: #E63E21; /* Cor desejada ao passar o mouse */
}

#finishedIcon:hover path {
  stroke: #0FF1A5;
}


.barStats{
  width: 4px;
  height: 25px;
  background-color: #E63E21;
  border-radius: 5px;
  margin-right: 16px;
}
</style>
