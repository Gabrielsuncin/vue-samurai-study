<template>
  <div class="container">
    <h2>Domínios</h2>
    <hr/>
    <b-container>
          <div class="form-todo form-group">
            <p>
              <input placeholder="Empresa:" class="form-control" type="text" v-model="compannies"/>
            </p>
            <p>
              <input placeholder="Domínio:" class="form-control" v-model="domain"/>
            </p>
            <button type="submit" class="btn btn-primary">Adicionar Domínio</button>
          </div>
      <hr/>
      <div class="list-group">
        <div class="list-group-item" v-for="companny in compannies" :key="companny.id">
          <span>Enpresa: <strong>{{ companny }}</strong></span>
          <p>Domínio: {{ domain }}</p>
          <div>
            <a href="#" title="Excluir">Excluir</a>
          </div>
        </div>
      </div>
      <hr/>
    </b-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      compannies: [],
      domain: [],
    };
  },
};
</script>
<style scoped>
.list-group-item {
  margin: 12px;
}
</style>
