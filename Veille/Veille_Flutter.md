📄 Veille_Flutter.md — Panorama des Frameworks Mobiles (2025)
I. Panorama des Frameworks Mobiles
1. Flutter (Google)

Flutter est un framework cross-platform lancé en 2017, basé sur le moteur de rendu Skia et le langage Dart. Depuis 2017, Flutter a évolué avec Flutter 3.x : support complet desktop, web, Material 3, Impeller (nouveau moteur de rendu) et meilleure performance. Il permet une UI cohérente et fluide sur mobile, web et desktop avec un seul codebase.

Plateformes supportées :

Mobile : Android, iOS

Web : Chrome, Firefox, Safari

Desktop : Windows, macOS, Linux

Embedded : Raspberry Pi, IoT (expérimental)

Nouveautés Flutter 3.x :

Material 3 + thèmes dynamiques

Impeller : rendu plus rapide et stable

WASM : exécution Web plus performante

Ajout d’améliorations DevTools et compilation plus rapide

Adoption (Flutter)

Selon SlashData 2024, Flutter est dans le top 3 des frameworks utilisés pour le mobile. Il est populaire dans la fintech, le retail, l’éducation et les apps gouvernementales. Exemples d’applications : BMW, Google Ads, ByteDance, Alibaba.

Forces / limites (Flutter)

Forces : UI cohérente, animations fluides, forte performance (AOT), productivité élevée (Hot Reload), vaste écosystème pub.dev.

Limites : taille des builds plus grande, intégrations natives parfois complexes, maîtrise de Dart nécessaire.

2. React Native (Meta)

React Native permet de créer des apps mobiles en JavaScript/TypeScript en s’appuyant sur des composants natifs. La New Architecture (Fabric + TurboModules) améliore fortement la performance en réduisant le bridge JS↔native. Expo facilite le développement rapide via des outils prêts à l’emploi.

Exemples d’entreprises : Instagram, Tesla, Shopify, Discord.

Comparaison communauté :
React Native a plus de packages NPM, Flutter a plus de packages spécialisés performants.

3. Kotlin Multiplatform (JetBrains)

KMP permet de partager la logique métier (business logic) en Kotlin tout en gardant une UI 100% native (SwiftUI + Jetpack Compose). Compose Multiplatform étend même la couche UI sur desktop et web.

Adoption : Utilisé par CashApp, McDonald’s, Philips, Netflix pour le partage de logique commune.
Limites : UI reste native → développement UI en double.
Forces : performance maximale, flexibilité, partage du code backend/mobile.

4. SwiftUI / UIKit & Jetpack Compose (Natif)

Les solutions natives offrent la meilleure performance, accès complet au hardware et intégration profonde aux APIs iOS/Android. SwiftUI et Compose augmentent fortement la productivité par rapport à UIKit/XML.

Limite : 2 bases de code → coût plus élevé, maintenance double.

5. Autres solutions hybrides

.NET MAUI / Xamarin : bon pour entreprises .NET mais communauté réduite.

Ionic / Capacitor : apps simples, basées WebView → limitées pour performance élevée.

Uno / Avalonia / NativeScript : niches (desktop-first, verticales spécifiques).

II. Architecture, performances & accès natif
Flutter

Moteur : Skia → Impeller (2024) pour moins de jank.

Compilation : AOT pour production (rapide), JIT pour Hot Reload.

Plateform Channels / FFI pour accéder au code natif (Swift, Kotlin, C++).

React Native

Fonctionne avec un bridge JS ↔ Natif.

Hermes améliore temps de démarrage et mémoire.

Kotlin Multiplatform

Compilation native (LLVM).

FPS dépend de SwiftUI/Compose.

III. Outils & workflow
Environnements

Flutter : Android Studio, VS Code

React Native : Expo, NodeJS, VS Code

KMP : IntelliJ, Android Studio

Gestion dépendances & packaging

pubspec.yaml (Flutter)

package.json (React)

Gradle/Kotlin (KMP)

IV. UX/UI & accessibilité
Design Systems

Flutter : Material 3, Cupertino

React Native : React Native Paper, NativeBase

Compose/SUI : thèmes dynamiques, animations fluides

Internationalisation

Flutter Intl, i18next, Kotlin resources

Support RTL, formats automatiques

V. Business, coûts & stratégie produit
Secteurs qui adoptent Flutter

Banque / fintech

Transport (BMW)

Retail (Alibaba)

Gouvernement

Apps internes/B2B

Coût & productivité

Flutter réduit le time-to-market : 1 seule équipe, un seul codebase.
React Native optimise via JS mais varie selon les libs.
KMP maximise qualité mais nécessite devs iOS/Android.

Communauté & roadmap

Flutter évolue rapidement (WASM, Impeller, Dart 3).
React Native mise sur la New Architecture.
KMP stabilisé depuis 2023.

📊 Tableau comparatif simplifié
Critère	Flutter	React Native	KMP	Natifs (SwiftUI/Compose)
Performance	⭐⭐⭐⭐	⭐⭐⭐	⭐⭐⭐⭐	⭐⭐⭐⭐⭐
Productivité	⭐⭐⭐⭐⭐	⭐⭐⭐⭐	⭐⭐⭐	⭐⭐⭐
Accès natif	⭐⭐⭐	⭐⭐⭐⭐	⭐⭐⭐⭐⭐	⭐⭐⭐⭐⭐
Communauté	⭐⭐⭐⭐	⭐⭐⭐⭐⭐	⭐⭐	⭐⭐⭐
Coût	⭐⭐⭐⭐⭐	⭐⭐⭐⭐	⭐⭐⭐	⭐⭐

📚 Sources

Stack Overflow Developer Survey 2024

SlashData Developer Nation 2024

Google I/O 2024

JetBrains KotlinConf 2024

Meta React Conf 2024
