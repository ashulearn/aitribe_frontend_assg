<template>
    <div>
    <style>
        .facet-container{
    width: 500px;
    }
    .right {
    float: right;
    }
    .left {
    float: left;
    }
    p {
    clear: both;
    padding-top: 1em;
    }
    .facet-list {
    list-style-type: none;
    margin: 0;
    padding: 0;
    margin-right: 10px;
    background: #eee;
    padding: 5px;
    width: 143px;
    min-height: 1.5em;
    font-size: 0.85em;
    }
    .facet-list li {
    margin: 5px;
    padding: 5px;
    font-size: 1.2em;
    width: 120px;
    }
    .facet-list li.placeholder {
    height: 1.2em
    }
    .facet {
    border: 1px solid #bbb;
    background-color: #fafafa;
    cursor: move;
    }
    .facet.ui-sortable-helper {
    opacity: 0.5;
    }
    .placeholder {
    border: 1px solid orange;
    background-color: #fffffd;
    }
    </style>
    <div class="facet-container">
  <div class="left">
    <label>Not Started</label>
    <ul id="notstarted" class="facet-list">
      <li class="facet" v-for="name in nsnames" :key="name"><nuxt-link to="add_ele">{{name.title}}</nuxt-link></li>
    </ul>
      <button><nuxt-link to="add_ele">new</nuxt-link></button>
  </div>
  
  <div class="right">
    <label>In Progress</label>
    <ul id="inprogress" class="facet-list">
      <li class="facet" v-for="name in ipnames" :key="name"><nuxt-link to="add_ele">{{name.title}}</nuxt-link></li>
    </ul>
  <button><nuxt-link to="add_ele">new</nuxt-link></button>
  </div>
  <div class="right">
    <label>Completed</label>
    <ul id="completed" class="facet-list">
      <li class="facet" v-for="name in cnames" :key="name"><nuxt-link to="add_ele">{{name.title}}</nuxt-link></li>
    </ul>
  <button><nuxt-link to="add_ele">new</nuxt-link></button>
  </div>
</div>
    </div>
    
</template>
<script>
  export default {
    data(){
      return {
        nsnames : [
          {title:'Card 4',description:'demo',status:'not started'},
          {title:'Card 1',description:'demo',status:'not started'},
          {title:'Card 5',description:'demo',status:'not started'}
        ],
        cnames : [
          {title:'Card 2',description:'demo',status:'complete'}
        ],
        ipnames : [
          {title : 'Card 3',description:'demo',status:'in progress'},
          {title : 'Card 6',description:'demo',status:'in progress'},
        ]
        

      }
    },
  }
</script>

