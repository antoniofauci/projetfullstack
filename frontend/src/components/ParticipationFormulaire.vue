<template>
  <div class="participation-form">
    <form>
      <div class="form-group">
        <label for="personne">Personne</label>
        <select id="personne" v-model="personne" class="form-control">
          <option value="personne1">Personne 1</option>
          <option value="personne2">Personne 2</option>
        </select>
      </div>
      <div class="form-group">
        <label for="projet">Projet</label>
        <select id="projet" v-model="projet" class="form-control">
          <option value="projet1">Projet 1</option>
          <option value="projet2">Projet 2</option>
        </select>
      </div>
      <div class="form-group">
        <label for="role">Rôle</label>
        <input type="text" id="role" v-model="role" class="form-control" />
      </div>
      <div class="form-group">
        <label for="pourcentage">Pourcentage</label>
        <input type="range" id="pourcentage" v-model="pourcentage" min="0" max="100" />
        <span>{{ pourcentage }}%</span>
      </div>
      <button type="submit" class="submit-button">Enregistrer</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const personne = ref('');
const projet = ref('');
const role = ref('');
const pourcentage = ref(0);
</script>

<style scoped>
.participation-form {
  max-width: 500px;
  margin: 30px auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  font-family: 'Arial', sans-serif;
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  font-weight: bold;
  margin-bottom: 8px;
  font-size: 14px;
  color: #333;
}

.form-control {
  width: 100%;
  padding: 10px;
  font-size: 14px;
  border: 1px solid #ddd;
  border-radius: 5px;
  box-sizing: border-box;
}

.submit-button {
  display: block;
  width: 100%;
  padding: 12px;
  font-size: 16px;
  color: white;
  background-color: #007bff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  text-align: center;
  transition: background-color 0.3s ease;
}

.submit-button:hover {
  background-color: #0056b3;
}

input[type="range"] {
  width: 100%;
  margin: 10px 0;
}

span {
  font-size: 14px;
  color: #555;
  display: block;
  text-align: center;
}
</style>
