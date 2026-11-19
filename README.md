# kGPS-Locator — Flutter 20: Geolocator

Projeto criado com `flutter create --empty --platforms=android,ios --project-name kgps_locator_kelvyn .` e desenvolvido conforme `material_base/Flutter-20-Geolocation.pdf`.

## Recursos desta aula

- Bússola visual que gira com o heading do sensor.
- Coordenadas e altitude fornecidas pelo GPS, com estados de espera e erro.
- Permissões de localização para Android e iOS.
- Lista inicial de três waypoints, cadastro de novos pontos usando a posição atual do GPS, navegação visual por toque longo, botão STOP e exclusão por gesto.
- Waypoints mantidos apenas em memória. Azimute e distância ainda são campos fictícios, conforme o fim do PDF; a navegação real ficou para a próxima aula.

## Executar

Use Flutter 3.50.0 ou versão compatível e um dispositivo Android/iOS com sensores, ou emulador com localização simulada:

```sh
flutter pub get
flutter run
```

No Android, conceda localização precisa durante o uso. Para simular posição no emulador, use **Extended Controls → Location → Set Location**. Para simular orientação, use **Virtual Sensors → Magnetic Field**.

## Verificações

```sh
flutter analyze
flutter test
```

O teste de interface cobre bloqueio sem GPS, navegação, exclusão, validação do nome, cadastro com posição GPS simulada e cancelamento. O teste de permissões e sensores reais exige dispositivo ou emulador configurado.

As respostas às perguntas da apostila estão em `RESPOSTAS.md`. O histórico Git mantém commits separados nos pontos solicitados pelo PDF.
