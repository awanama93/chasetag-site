### Struktur Permainan

- Satu sesi permainan terdiri atas 5 [[CoreMechanic#^ronde|ronde]]
- Sebelum sesi dimulai, dilakukan pengacakan apa [[CoreMechanic#^role|role]] dari player character maupun AI character
- ##### Timer
  - 1 ronde dilaksanakan selama 2 menit (real-life time)^ronde

#### End condition

- paling lambat, permainan selesai jika sudah dilakukan 5 [[CoreMechanic#^ronde|ronde]] ^end-condition
- tetapi permainan bisa dinyatakan selesai jika ada satu character yang sudah memenangkan 3 [[CoreMechanic#^ronde|ronde]]
- #### Round win condition
  - Character menang di suatu ronde jika berhasil memenuhi objective dari [[CoreMechanic#^role|role]]-nya pada ronde tersebut
  - Jika menang, maka score character tersebut bertambah 1

* #### Round lose condition
  - Character kalah di suatu ronde jika gagal memenuhi objective dari [[CoreMechanic#^role|role]]-nya pada ronde tersebut

#### Role

- #### Chaser
  - Chaser adalah role di mana character harus melakukan tag pada lawan untuk memenangkan ronde ^role
  - Character yang memiliki role chaser menang pada suatu ronde jika dia berhasil melakukan tag terhadap character lawan sebelum ronde berakhir ^chaser
  - Chaser bisa melakukan [[CoreMechanic#^tagging|tagging]]
- #### Evader
  - Evader adalah role di mana character harus menghindari tag dari lawan selama ronde berlangsung ^evader
  - Character yang memiliki role evader menang pada suatu ronde jika dia berhasil tidak dikenai tag oleh character lawan sampai ronde berakhir
  - Evader tidak bisa melakukan [[CoreMechanic#^tagging|tagging]]

### Character

- Untuk memenangkan permainan, character (baik player character maupun AI character) bisa melakukan beragam jenis movement.
  - Ketika melakukan [[CoreMechanic#^movement|movement]], character menggunakan stamina

  - Selama permainan berlangsung, character bisa mendapatkan buff & nerf dari menyentuh token buff & nerf yang dimunculkan secara sembarang di wilayah arena dalam interval tertentu ^movement

  - #### Movement
    - ##### Walk
      - Character bisa berjalan (walk) dengan kecepatan normal ^walk
      - Character bisa berjalan (walk) maju maupun mundur
      - Walk tidak mengurangi stamina
      - Jika character melakukan walk, maka [[CoreMechanic#^stamina|stamina]] bertambah seiring waktu
    - ##### Strafing
      - Character bisa melakukan strafing (berjalan ke samping tanpa mengubah pandangan) ^strafing
      - Character bisa melakukan strafing dengan kecepatan normal
      - Jika character melakukan strafing, maka [[CoreMechanic#^stamina|stamina]] bertambah seiring waktu
    - ##### Sprint
      - Character bisa berlari (sprint) ^sprint
      - Berlari (sprint) berarti melaju dengan kecepatan bertambah secara bertahap
      - Character bisa berlari (sprint) maju
      - Jika character melakukan sprint, maka [[CoreMechanic#^stamina|stamina]] berkurang selama sprint dilakukan
      - Character bisa melakukan sprint selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan sprint
    - ##### Jump
      - Character bisa melompat (jump) ^jump
      - Daya lompat character dipengaruhi oleh kecepatan lajunya. Semakin cepat lajunya, semakin jauh atau tinggi lompatannya
      - Character bisa melompat ke depan, belakang, kiri, kanan
      - Jika character melakukan jump, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika jump dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah menjejak tanah kembali
      - Character bisa melakukan jump selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan jump
    - ##### Slide
      - Character bisa melakukan slide ^slide
      - Slide berarti character menjatuhkan badan dan meluncurkan tubuhnya
      - Character bisa melakukan slide ke depan dan samping, tidak bisa ke belakang
      - Ketika character melakukan slide, terjadi penambahan kecepatan yang lumayan drastis dalam waktu singkat, lalu melambat kembali ke kecepatan normal ketika slide berakhir
      - Slide bisa digunakan untuk melewati [[CoreMechanic#^obstacle|obstacle]] dengan celah yang ketinggiannya lebih rendah dari pinggang character. Jadi character melakukan slide untuk masuk dan melewati celah dari [[CoreMechanic#^obstacle|obstacle]] tersebut
      - Tetapi slide bisa juga dilakukan di mana pun
      - Jika character melakukan slide, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika slide dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
      - Character bisa melakukan slide selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan slide
    - ##### Vault
      - Character bisa melakukan vault ^vault
      - Character bisa melakukan vault ke depan
      - Vault berarti character menggunakan tangannya untuk meraih permukaan yang setidaknya lebih tinggi dari pinggangnya, lalu menarik badannya dan meluncur di atas permukaan tersebut
      - Jika character melakukan vault, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika vault dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
      - Character bisa melakukan vault selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan vault
    - ##### Climb
      - Character bisa memanjat (climb) ^climb
      - Climb berarti character menggunakan tangannya untuk meraih permukaan lebih tinggi dari badan, lalu mengangkat tubuhnya sehingga bisa character menaik ke puncak permukaan tersebut
      - Jika character melakukan climb, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika climb dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
      - Character bisa melakukan climb selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan climb
    - ##### Tic tac
      - Character bisa melakukan tic tac ^tic-tac
      - Tic tac berarti character melompat mengarah ke tembok, lalu menggunakan permukaan tembok tersebut sebagai titik pijak lagi untuk melompat ke arah lain
      - Perubahan arah lompatan ketika character melakukan tic tac secara otomatis dikalkulasi berdasarkan sudut tabrakan character dengan tembok. Misalnya, jika character menabrak tepat dari lurus depan tembok, maka otomatis dia akan melakukan tic tac ke arah sebaliknya (meninggalkan tembok). Lalu, jika character menabrak tembok agak lebih dari sisi kiri tembok, maka tic tac-nya akan lebih memantul ke kanan
      - Jika character melakukan tic tac, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika tic tac dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah memijak tanah lagi
      - Character bisa melakukan tic tac selama masih memiliki [[CoreMechanic#^stamina|stamina]] ketika dia melakukan [[CoreMechanic#^jump|jump]]
    - ##### Pole spin
      - Character bisa melakukan pole spin ^pole-spin
      - Pole spin berarti character menggunakan tangannya untuk meraih vertical pole yang ada di dekatnya lalu memutarkan badannya dengan menggunakan pole tersebut sebagai poros
      - Putaran pada pole spin bisa full (360 derajat) atau tidak full (hanya berputar sedikit, misalnya)
      - Jika character melakukan pole spin, maka [[CoreMechanic#^stamina|stamina]] berkurang selama pole dilakukan. Jadi, [[CoreMechanic#^stamina|stamina]] bisa berkurang sedikit jika putaran tidak dilakukan sebanyak 360 derajat, misalnya.
    - ##### Wall rebound
      - Character bisa melakukan wall rebound ^wall-rebound
      - Wall rebound berarti character melaju lalu menabrak tembok lalu mengubah arah lajunya
      - Wall rebound dilakukan secara otomatis ketika character melaju dalam kecepatan tertentu lalu menabrak dengan tembok
      - Perubahan arah laju secara otomatis dikalkulasi berdasarkan sudut tabrakan character dengan tembok. Misalnya, jika character menabrak tepat dari lurus depan tembok, maka otomatis dia akan melakukan wall rebound ke arah sebaliknya (meninggalkan tembok). Lalu, jika character menabrak tembok agak lebih dari sisi kiri tembok, maka wall reboundnya akan lebih memantul ke kanan
      - Jika character melakukan wall rebound, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika wall rebound dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali

  - #### Tagging
    - Character bisa melakukan tagging terhadap character lain ^tagging
    - Tagging berarti character menyemprotkan sesuatu terhadap character lawan
    - Secara default, area of effect dari semprotan tag itu seperti cone
    - Secara default, jarak semprotan tag tidak begitu jauh
    - Jika character dengan role [[CoreMechanic#^role|evader]] bertabrakan dengan semprotan tag dari character [[CoreMechanic#^role|chaser]]
    - Character [[CoreMechanic#^role|evader]] bisa dikenai tag ketika melakukan movement apa pun selama semprotan tag bertabrakan dengannya
    - Hanya character [[CoreMechanic#^role|chaser]] yang bisa melakukan aksi tagging
    - Jika character melakukan tagging, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika tagging dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character berhenti melakukan tagging

  - #### Stamina system
    - Character menggunakan stamina untuk melakukan beragam [[CoreMechanic#^movement|movement]] ^stamina
    - Player bisa melihat stamina point player character melalui indikator stamina pada layer user interface
    - Player bisa melihat indikator stamina AI character yang terdapat pada atas character
    - Jika stamina character mencapai 0, maka character masuk ke dalam kondisi exhausted
    - Exhausted adalah kondisi di mana kecepatan character 0.6x kecepatan normal dan character tidak bisa melakukan aksi selain [[CoreMechanic#^walk|walk]] atau [[CoreMechanic#^strafing|strafing]] sampai stamina mencapai nilai maksimal. Kondisi exhausted akan berhenti begitu stamina character mencapai nilai maksimal. ^exhausted
    - ##### Base stamina cost
      - Berikut ini adalah nilai dasar stamina point yang dibutuhkan untuk melakukan suatu aksi. **PERHATIAN:** programmer dan tim sangat dianjurkan untuk melakukan penyesuaian nilai ini untuk meningkatkan game feel dan game balance dari game ini. Ini hanya sebagai nilai dasar.
      - ![[BaseStaminaCostTable |Stamina Cost Table]]

  - #### Buff & Nerf
    - Sepanjang ronde di wilayah arena akan dimunculkan beragam buff dan nerf token ^buff-nerf
    - Token buff dan nerf adalah token yang akan mengubah nilai stat dari character selama beberapa saat. Jadi perubahannya tidak permanen.
    - Player bisa melihat buff atau nerf apa yang sedang dimiliki player character lewat informasi di user interface
    - Player bisa melihat buff atau nerf apa yang sedang dimiliki AI character lewat informasi simbol yang ada di atas AI character
    - Untuk mengaktifkan token buff dan nerf, character hanya perlu menabrak token tersebut
    - Token buff dan nerf dimunculkan dengan interval per 20 detik sekali
    - Pada satu kali pemunculan token buff & nerf, total token yang dimunculkan adalah 5
    - Pada satu kali pemunculan token buff & nerf, hanya boleh ada 1 token untuk satu buff/nerf token. Misalnya, hanya ada 1 token speed up pada satu kali pemunculan token buff & nerf
    - Ketika suatu interval pemunculan token buff dan nerf selesai, maka token buff dan nerf yang sebelumnya ada di arena dihilangkan terlebih dahulu. Lalu, token buff dan nerf baru dimunculkan. Jadi, tidak akan ada penumpukan token buff dan nerf
    - ![[BuffNerfTokenTable]]

### Arena

- #### Level design
  - Layout dari level design untuk game ini sepenuhnya didasarkan pada The Quad dari World Chase Tag
    - [Cek layout The Quad dalam bentuk 2D di sini](https://www.chasealphen.nl/en/wct/)
    - ![[Asset/TheQuad2D.png]]
    - [Cek layout The Quad dalam bentuk 3D di sini](https://sketchfab.com/3d-models/world-chase-tag-quad-98a0579a56b24a30ad83f9b7b93f0fd4)
    - ![[Asset/TheQuad3D.png]]
  - **PERHATIAN:** tetapi, tim development bisa memodifikasi **detail** dari layout ini.
- #### Obstacle
  - Obstacle adalah benda-benda dalam arena yang bisa diinteraksi oleh character ^obstacle
  - **PERHATIAN:** tim bisa menggunakan beragam obstacle
