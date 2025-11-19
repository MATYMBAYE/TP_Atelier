Panorama des Frameworks Mobiles (2025)
I. Kotlin Multiplatform (JetBrains)
1. Concept

Objectif : partager la logique métier (business logic, networking, data storage) entre plusieurs plateformes (iOS, Android, desktop, backend) tout en gardant une UI native sur chaque OS.

Compilation multiplateforme : le code Kotlin “common” est compilé en bytecode JVM, Swift ou JavaScript selon la cible.

UI : Compose Multiplatform permet d’écrire du code UI réutilisable, mais pour UI très avancée, il est souvent préférable d’utiliser SwiftUI / Jetpack Compose natif.

Exemple concret : une app iOS et Android partage 80% du code métier, mais chaque app a son UI optimisée nativement.

2. Architecture

Code common → logique métier, modèles de données, network.

Code platform-specific → accès aux APIs natives, UI.

Interopérabilité : Kotlin → Swift / Kotlin → JS pour web, etc.

Schéma slide :

[Common Code (Kotlin)] 
      ↓
--------------------------
| iOS (SwiftUI)          |
| Android (Jetpack Compose) |
--------------------------

3. Performances

Compilation directe en code natif → UI fluide, FPS élevé.

Pas de bridge JS → moins de latence comparé à React Native.

Idéal pour apps complexes avec logique métier lourde (ex : finance, santé, IoT).

4. Accès natif & plugins

Peut utiliser toutes les APIs natives (HealthKit, CarPlay, Bluetooth, WearOS).

KMP ne fournit pas un écosystème “plugins” comme Flutter → développeur peut écrire des wrappers Kotlin → Swift/ObjC pour iOS.

Très flexible mais demande expertise Kotlin et plateforme cible.

5. Adoption / Cas d’usage

Entreprises : CashApp, Philips, McDonalds.

Cas d’usage : apps mobiles avec logique métier partagée, backend multiplateforme, IoT apps.

Limites : UI 100% native souvent nécessaire → double maintenance si on veut une interface complexe sur toutes plateformes.

6. Points forts / limites
Points forts	Limites
Partage logique métier efficace	UI complexe nécessite natif
Performance proche du natif	Petite communauté comparée à Flutter/React Native
Accès complet aux APIs natives	Besoin compétences Kotlin + plateformes
7.Faiblesses

UI native souvent nécessaire : Compose Multiplatform existe mais n’est pas encore aussi mature que SwiftUI/Jetpack Compose.

Petite communauté : moins de packages et de support comparé à Flutter ou React Native.

Courbe d’apprentissage : nécessite compétences en Kotlin et connaissance des plateformes cibles (iOS/Android).

Maintenance multiple : si UI complexe → deux bases de code UI à maintenir.
Sources à citer pour la slide :

Kotlin Multiplatform Documentation

JetBrains Blog / Compose Multiplatform updates 2024-2025

Exemples entreprises : CashApp, Philips (articles Medium / Dev blogs)