<template>
  <div>
    <div id="slogan" class="text-center">
      <h1>NameGator</h1>
      <h6 class="text-secondary">Gerador de nomes ultilizando Vue.js, GraphQL e Node</h6>
    </div>
    <div id="main">
      <div class="container">
        <div class="row">
          <div class="col-md">
            <h5>
              Prefixos
              <span class="badge badge-info">{{prefixes.length}}</span>
            </h5>
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li class="list-group-item" v-for="prefix in prefixes" v-bind:key="prefix">{{prefix}}</li>
                  
                </ul>
                <br />
                <input class="form-control" type="text" placeholder="Digiteo sufixo" />
              </div>
            </div>
          </div>
          <div class="col-md">
            <h5>
              Sufixos
              <span class="badge badge-info">{{sufixes.length}}</span>
            </h5>
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li class="list-group-item" v-for="sufis in sufixes" v-bind:key="sufis">{{sufis}}</li>
                  
                </ul>
                <br />
                <input class="form-control" type="text" placeholder="Digiteo sufixo" />
              </div>
            </div>
          </div>
        </div>
        <h5>Domínios <span class="badge badge-info">{{domains.length}}</span></h5>
        <div class=" card">
          <div class="card-body">
            <ul class="list-group">
              <li class="list-group-item" v-for="domain in domains" v-bind:key="domain.name">{{domain}}</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import "font-awesome/css/font-awesome.css";
export default {
  name: "app",
  data: () => {
    return {
      prefixes: ['Air','Jet','Fligth'],
      sufixes: ['Hub', 'Station','Mart'],
      domains:['Air','Jet','Fligth','Hub', 'Station','Mart']
    };
  }
};
</script>

<style>
#slogan {
  margin-top: 30px;
  margin-bottom: 30px;
}

#main {
  background-color: #f1f1f1;
  padding-top: 30px;
  scroll-padding-bottom: 30px;
}
</style>
