<script>
  import { FirebaseApp } from "sveltefire";
  import firebase from "firebase/app";
  import "firebase/firestore";
  import "firebase/auth";
  import "firebase/storage";
  import "firebase/performance";
  import "firebase/analytics";

  const firebaseConfig = {
    apiKey: "AIzaSyCMJrVLEjg9F64db3yg-LWwfi8-nhnNFyA",
    authDomain: "reactcards-8111e.firebaseapp.com",
    databaseURL: "https://reactcards-8111e.firebaseio.com",
    projectId: "reactcards-8111e",
    storageBucket: "reactcards-8111e.appspot.com",
    messagingSenderId: "690332166599",
    appId: "1:690332166599:web:868f116b4155631bc0d1e2",
    measurementId: "G-B1QXFJ8YFD",
  };

  firebase.initializeApp(firebaseConfig);
</script>

<FirebaseApp {firebase}>
  <slot />
</FirebaseApp>
