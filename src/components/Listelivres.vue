<template>
  <div>
    <!--  <button class="btn btn-success" @click="ajouter">Nouveau</button>

    <form action="">
      ISBN du livre : {{ liv.isbn }} <input type="text" v-model="liv.isbn" placeholder="  ISBN">
      Titre du livre : {{ liv.titre }}<input type="text" v-model="liv.titre" placeholder="Titre">
      Auteur du livre : {{ liv.auteur }}<input type="text" v-model="liv.auteur" placeholder="Auteur">
      Année Edition du livre : {{ liv.annedition }}<input type="date" v-model="liv.annedition"
        placeholder="Année Eddition">
      Prix du livre : {{ liv.prix }}<input type="number" v-model="liv.prix" placeholder="Prix">
      Couverture du livre : {{ liv.couverture }}<input type="text" v-model="liv.couverture" placeholder="Couverture">
    </form><div> -->

    <button class="btn btn-success" @click="ajouter">Nouveau</button>

    <form action="" class="book-form">
      <div class="form-group">
        <label for="isbn">ISBN du livre:</label>
        <input type="text" id="isbn" v-model="liv.isbn" placeholder="ISBN">

        <label for="titre">Titre du livre:</label>
        <input type="text" id="titre" v-model="liv.titre" placeholder="Titre">

        <label for="auteur">Auteur du livre:</label>
        <input type="text" id="auteur" v-model="liv.auteur" placeholder="Auteur">

        <label for="annedition">Année Edition du livre:</label>
        <input type="date" id="annedition" v-model="liv.annedition" placeholder="Année Edition">

        <label for="prix">Prix du livre:</label>
        <input type="number" id="prix" v-model="liv.prix" placeholder="Prix">

        <label for="couverture">Couverture du livre:</label>
        <input type="text" id="couverture" v-model="liv.couverture" placeholder="Couverture">
      </div>
    </form>

    <table class="table table-striped">
      <th>Couverture</th>
      <th>ISBN</th>
      <th>Titre</th>
      <th>Auteur</th>
      <th>Année Edition</th>
      <th>Prix</th>
      <th>Modifier</th>
      <th>Supprimer</th>
      <tbody>
        <tr v-for="liv in livres" :key="liv.isbn">
          <td><img :src="liv.couverture" height="70" width="70"></td>
          <td>{{ liv.isbn }}</td>
          <td>{{ liv.titre }}</td>
          <td>{{ liv.auteur }}</td>
          <td>{{ liv.annedition }}</td>
          <td>{{ liv.prix }}</td>
          <td><button class="btn btn-warning">Modifier</button></td>
          <td><button class="btn btn-danger">Supprimer</button></td>
        </tr>
      </tbody>

    </table>
  </div>
</template>

<script setup>
import { ref } from "vue";
const livres = ref([
  {
    isbn: "42368756",
    titre: "ReactJS",
    auteur: "Romain Rissouan",
    annedition: 2021,
    prix: 33,
    couverture: "https://m.media-amazon.com/images/I/61vg+0-1yGL._SY466_.jpg",
  },
  {
    isbn: "123698745",
    titre: "Les VPNS",
    auteur: "Stephan@gmail.com",
    annedition: 2020,
    prix: 55,
    couverture:
      "http://res.cloudinary.com/iset-sfax/image/upload/v1696761358/images/9782100491155_internet_w290.jpg.jpg",
  },
  {
    isbn: "54894",
    titre: "Techniques de Référencement Web",
    auteur: "Patrick Wampe",
    annedition: 2020,
    prix: 55,
    couverture:
      "https://blog.internet-formation.fr/wp-content/uploads/2018/04/1e-4e-couverture-livre-SEO.jpg",
  },
  {
    isbn: "5464sf",
    titre: "VueJS",
    auteur: "Alexandra Martin",
    annedition: 2020,
    prix: 20,
    couverture: "https://m.media-amazon.com/images/I/718QqTspltL._SY466_.jpg",
  },
  {
    isbn: "65465445",
    titre: "Laravel",
    auteur: "Eric Sarrion",
    annedition: 2020,
    prix: 50,
    couverture: "https://images.booksense.com/images/132/218/9798554218132.jpg",
  },
]);

const liv = {
  isbn: "",
  titre: "",
  auteur: "",
  annedition: "",
  prix: "",
  couverture: "",
};

const ajouter = () => {
  const l1 = {
    isbn: liv.isbn,
    titre: liv.titre,
    auteur: liv.auteur,
    annedition: liv.annedition,
    prix: liv.prix,
    couverture: liv.couverture,
  };

  livres.value.push(l1);
};
</script>

<style lang="scss" scoped>
.book-form {
  max-width: 400px;
  margin: auto;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: none;
  font-weight: 500;
  margin-bottom: 5px;
}

input {
  width: 50%;
  height: 0.5cm;
  padding: 8px;
  box-sizing: border-box;
}

th {
  font-size: x-large;

}
</style>