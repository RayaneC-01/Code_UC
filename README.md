# Diagramme d'Utilisation

```plantuml
@startuml
left to right direction
actor Utilisateur

|Application|
rectangle Application {
  usecase "Contrôler la lumière" as UC1
  usecase "Gérer la batterie" as UC2
  usecase "Programmer des horaires" as UC3
  usecase "Recevoir des notifications" as UC4
  usecase "Mettre à jour le firmware" as UC5
  usecase "S'inscrire" as UC6
  usecase "Se connecter" as UC7
}

Utilisateur -> UC6 : <<extend>>
Utilisateur -> UC7
Utilisateur -> UC1
Utilisateur -> UC2
Utilisateur -> UC3
Utilisateur -> UC4
Utilisateur -> UC5

UC1 -> UC4 : <<include>>
UC2 -> UC4 : <<include>>
UC3 -> UC1 : <<include>>
UC5 -> UC7 : <<include>>
@enduml