# TP : Création de la Page d’Accueil d’un Site Web avec Bootstrap
## Objectif du TP
Dans ce TP, vous allez créer la première page d’un site web moderne en utilisant  :
- **HTML5**
- **CSS**
- **Bootstrap 5**

Les composants interactifs (menu responsive, slider…) sont gérés automatiquement par Bootstrap.

--- ---

# Importer Bootstrap dans le fichier `index.html`

Ajoutez ce code dans la balise `<head>` :

```html
<!-- Bootstrap CSS -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">

<!-- Bootstrap JS (nécessaire pour le slider et la navbar mobile) -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

Explication

Le premier lien charge le design Bootstrap (couleurs, layout…).

Le script charge le fonctionnement des composants (ex. slider, navbar burger).

Créer la barre de navigation (Navbar)

Ajoutez ce code dans <body> :

<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="container">
    <a class="navbar-brand" href="#">MySite</a>

    <button class="navbar-toggler" type="button"
      data-bs-toggle="collapse" data-bs-target="#menu">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="menu">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="#">Accueil</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Événements</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Produits</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
      </ul>
    </div>
  </div>
</nav>

# Explication

navbar-expand-lg → menu étendu sur grands écrans.

navbar-dark bg-primary → thème sombre + fond bleu.

navbar-toggler → bouton burger sur mobile.

collapse navbar-collapse → masque le menu sur petit écran.

ms-auto → aligne le menu à droite.

Slider / Carousel Bootstrap

Ajoutez ce composant :

<div id="heroSlider" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">

    <div class="carousel-item active">
      <img src="https://picsum.photos/1200/400?1" class="d-block w-100">
    </div>

    <div class="carousel-item">
      <img src="https://picsum.photos/1200/400?2" class="d-block w-100">
    </div>

    <div class="carousel-item">
      <img src="https://picsum.photos/1200/400?3" class="d-block w-100">
    </div>

  </div>

  <button class="carousel-control-prev" type="button"
   data-bs-target="#heroSlider" data-bs-slide="prev">
    <span class="carousel-control-prev-icon"></span>
  </button>

  <button class="carousel-control-next" type="button"
   data-bs-target="#heroSlider" data-bs-slide="next">
    <span class="carousel-control-next-icon"></span>
  </button>
</div>

Explication

carousel slide → active le slider.

data-bs-ride="carousel" → défile automatiquement.

carousel-item active → première image affichée.

Les flèches prev/next sont intégrées par Bootstrap.

Section “Nos Événements” (3 cartes Bootstrap)

<section class="container my-5">
  <h2 class="text-center mb-4">Nos Événements</h2>

  <div class="row g-4">

    <div class="col-md-4">
      <div class="card">
        <img src="https://picsum.photos/300/180?event1" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title">Événement 1</h5>
          <p class="card-text">Description courte de l’événement.</p>
          <a href="#" class="btn btn-primary">Lire plus</a>
        </div>
      </div>
    </div>

    <div class="col-md-4">
      <div class="card">
        <img src="https://picsum.photos/300/180?event2" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title">Événement 2</h5>
          <p class="card-text">Description courte de l’événement.</p>
          <a href="#" class="btn btn-primary">Lire plus</a>
        </div>
      </div>
    </div>

    <div class="col-md-4">
      <div class="card">
        <img src="https://picsum.photos/300/180?event3" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title">Événement 3</h5>
          <p class="card-text">Description courte de l’événement.</p>
          <a href="#" class="btn btn-primary">Lire plus</a>
        </div>
      </div>
    </div>

  </div>
</section>


Explication

container → marges automatiques.

row g-4 → grille + espace entre colonnes.

col-md-4 → 3 colonnes sur écrans moyens et grands.

card → composant Bootstrap prêt à l’emploi.

# Section “Nos Produits” (3 cartes avec prix)

<section class="container my-5">
  <h2 class="text-center mb-4">Nos Produits</h2>

  <div class="row g-4">

    <div class="col-md-4">
      <div class="card">
        <img src="https://picsum.photos/300/180?product1" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title">Produit 1</h5>
          <p class="text-success fw-bold">250 DH</p>
          <a href="#" class="btn btn-success">Acheter</a>
        </div>
      </div>
    </div>

    <div class="col-md-4">
      <div class="card">
        <img src="https://picsum.photos/300/180?product2" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title">Produit 2</h5>
          <p class="text-success fw-bold">350 DH</p>
          <a href="#" class="btn btn-success">Acheter</a>
        </div>
      </div>
    </div>

    <div class="col-md-4">
      <div class="card">
        <img src="https://picsum.photos/300/180?product3" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title">Produit 3</h5>
          <p class="text-success fw-bold">150 DH</p>
          <a href="#" class="btn btn-success">Acheter</a>
        </div>
      </div>
    </div>

  </div>
</section>

Explication

Section identique à “Événements”.

text-success fw-bold → prix vert + gras.

btn-success → bouton vert Bootstrap.

# Footer
<footer class="bg-dark text-white text-center p-3 mt-5">
  <p>© 2025 MySite - Tous droits réservés</p>
  <p>
    <a href="#" class="text-white text-decoration-none me-3">Accueil</a>
    <a href="#" class="text-white text-decoration-none">Contact</a>
  </p>
</footer>

Explication

bg-dark text-white → thème sombre.

p-3 → padding.

text-decoration-none → supprime le soulignement des liens.

#Style CSS personnalisé
Ajoutez dans style.css :

h2 {
  font-weight: 700;
  color: #0d6efd;
}

.card img {
  height: 180px;
  object-fit: cover;
}

Explication

Met les titres en bleu + gras.

Ajuste les images pour qu’elles gardent un bon cadrage.





