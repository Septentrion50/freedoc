# Freedoc

Pour paramétrer la base de données voici la marche à suivre :

- Faire un `bundle install`
- Ensuite, rentre la commande `rails db:migrate`
- Puis, lancer `rails db:seed`

## Si vous voulez tester

Voici un bref rappel des commandes possibles

Notez que le code postal du praticien est inclus dans la table `cities` (c'était plus logique).

|Action|Commande|
|:---|:---|
|Afficher la table des Rendez-vous|`tp Appointment.all`|
|Créer une ville|`City.create(name: "nom de la ville", zip_code: code postal)`|
|Créer une spécialité|`Speciality.create(name: "nom de la spécialité")`|
|Créer un nouveau praticien|`Doctor.create(first_name: "prénom", last_name: "nom de famille", city: City.find_by(name: nom de la ville)`)|
|Ajouter une spécialité à un praticien|`d = Doctor.find(id du docteur)` puis `d.specialities << Speciality.find_by(name: nom_de_la_specialité)`|
|Créer un patient|`Patient.create(first_name: prénom du patient, last_name: nom du patient, city: City.find_by(name: nom de la ville))`|
|Créer un rendez-vous|`Appointment.create(date: YYYY-mm-DD HH:MM:SS, doctor: praticen_existant, patient: patient_existant)`|

