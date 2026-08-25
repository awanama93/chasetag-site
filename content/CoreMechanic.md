<div id="struktur-permainan"></div>
### Struktur Permainan
- Satu sesi permainan terdiri atas 5 [[CoreMechanic#^ronde|ronde]] ^struktur-permainan
- Sebelum sesi dimulai, dilakukan pengacakan apa [[CoreMechanic#^role|role]] dari player character maupun AI character, siapa yang menjadi [[CoreMechanic#^chaser|chaser]] dan siapa yang menjadi [[CoreMechanic#^evader|evader]]
- ##### Timer
	-  1 ronde dilaksanakan selama 2 menit (real-life time)^ronde

<div id="end-condition"></div>
#### End condition
* paling lambat, permainan selesai jika sudah dilakukan 5 [[CoreMechanic#^ronde|ronde]] ^end-condition
* tetapi permainan bisa dinyatakan selesai jika ada satu character yang sudah memenangkan 3 [[CoreMechanic#^ronde|ronde]]
* #### Round win condition
	- Character menang di suatu ronde jika berhasil memenuhi objective dari [[CoreMechanic#^role|role]]-nya pada ronde tersebut
	- Jika menang, maka score character tersebut bertambah 1
- #### Round lose condition
	* Character kalah di suatu ronde jika gagal memenuhi objective dari [[CoreMechanic#^role|role]]-nya pada ronde tersebut

<div id="role"></div>
#### Role
- #### Chaser
	* Chaser adalah role di mana character harus melakukan [[CoreMechanic#^tagging|tagging]] pada lawan untuk memenangkan ronde ^role
	* Character yang memiliki role chaser menang pada suatu [[CoreMechanic#^ronde|ronde]] jika dia berhasil melakukan [[CoreMechanic#^tagging|tagging]] terhadap character lawan sebelum ronde berakhir ^chaser
	* Chaser bisa melakukan [[CoreMechanic#^tagging|tagging]] 
- #### Evader
	* Evader adalah role di mana character harus menghindari [[CoreMechanic#^tagging|tagging]] dari lawan selama ronde berlangsung ^evader
	* Character yang memiliki role evader menang pada suatu [[CoreMechanic#^ronde|ronde]] jika dia berhasil tidak dikenai [[CoreMechanic#^tagging|tagging]] oleh character lawan sampai ronde berakhir
	* Evader tidak bisa melakukan [[CoreMechanic#^tagging|tagging]] 

### Character

- Untuk memenangkan permainan, character (baik player character maupun AI character) bisa melakukan beragam jenis movement.

  - Ketika melakukan [[CoreMechanic#^movement|movement]], semua character menggunakan stamina
  - Semua character bisa melakukan [[CoreMechanic#^tagging|tagging]] ketika mendapatkan giliran sebagai [[CoreMechanic#^chaser|chaser]]
  - Selama permainan berlangsung, semua character bisa mendapatkan buff & nerf dari menyentuh [[CoreMechanic#^buff-nerf|token buff & nerf]] yang dimunculkan secara sembarang di wilayah arena dalam interval tertentu ^movement
  - #### Jenis Character
    - Player character
      - Player character adalah character yang dikendalikan oleh player ^player-character
    - AI character
      - AI character adalah character yang dikendalikan oleh computer/AI. Arahan tentang pengambilan keputusan AI dideskripsikan pada bagian [[CoreMechanic#^decision|decision]]
  - #### Movement
    - Penjelasan tentang cara player melakukan kontrol player character, dijelaskan di bagian [[CoreMechanic#^interaction|interaction]]
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
      - Referensi gerakan slide:
      - ![](https://youtu.be/9nc7lD4c8-Q?si=5xlM7xxdDbCz_b6E)
    - ##### Vault
      - Character bisa melakukan vault ^vault
      - Character bisa melakukan vault ke depan
      - Vault berarti character menggunakan tangannya untuk meraih permukaan yang setidaknya lebih tinggi dari pinggangnya, lalu menarik badannya dan meluncur di atas permukaan tersebut
      - Jika character melakukan vault, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika vault dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
      - Character bisa melakukan vault selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan vault
      - Referensi gerakan vault:
      - ![](https://youtu.be/f65H4Rr0oD0?si=uq5REzPnb6qh22Pn)
    - ##### Climb
      - Character bisa memanjat (climb) ^climb
      - Climb berarti character menggunakan tangannya untuk meraih permukaan lebih tinggi dari badan, lalu mengangkat tubuhnya sehingga bisa character menaik ke puncak permukaan tersebut
      - Jika character melakukan climb, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika climb dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
      - Character bisa melakukan climb selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan climb
      - Referensi gerakan climb:
      - ![](https://youtu.be/UEIU3uTkczQ?si=GiK_8s9e9bIySK_Y)
    - ##### Tic tac
      - Character bisa melakukan tic tac ^tic-tac
      - Tic tac berarti character melompat mengarah ke tembok, lalu menggunakan permukaan tembok tersebut sebagai titik pijak lagi untuk melompat ke arah lain
      - Perubahan arah lompatan ketika character melakukan tic tac secara otomatis dikalkulasi berdasarkan sudut tabrakan character dengan tembok. Misalnya, jika character menabrak tepat dari lurus depan tembok, maka otomatis dia akan melakukan tic tac ke arah sebaliknya (meninggalkan tembok). Lalu, jika character menabrak tembok agak lebih dari sisi kiri tembok, maka tic tac-nya akan lebih memantul ke kanan
      - Jika character melakukan tic tac, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika tic tac dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah memijak tanah lagi
      - Character bisa melakukan tic tac selama masih memiliki [[CoreMechanic#^stamina|stamina]] ketika dia melakukan [[CoreMechanic#^jump|jump]]
      - Referensi gerakan tic tac:
      - ![](https://youtu.be/Uh5ha6dUV8o?si=0b185RSyGwzEHAKB)
    - ##### Pole spin
      - Character bisa melakukan pole spin ^pole-spin
      - Pole spin berarti character menggunakan tangannya untuk meraih vertical pole yang ada di dekatnya lalu memutarkan badannya dengan menggunakan pole tersebut sebagai poros
      - Putaran pada pole spin bisa full (360 derajat) atau tidak full (hanya berputar sedikit, misalnya)
      - Jika character melakukan pole spin, maka [[CoreMechanic#^stamina|stamina]] berkurang selama pole dilakukan. Jadi, [[CoreMechanic#^stamina|stamina]] bisa berkurang sedikit jika putaran tidak dilakukan sebanyak 360 derajat, misalnya.
      - Referensi gerakan pole spin:
      - ![](https://youtu.be/6_S6P8_3hX4?si=r0LardJ6wXTEiGIt)
    - ##### Wall rebound
      - Character bisa melakukan wall rebound ^wall-rebound
      - Wall rebound berarti character melaju lalu menabrak [[CoreMechanic#^wall|wall]] lalu mengubah arah lajunya
      - Wall rebound dilakukan secara otomatis ketika character melaju dalam kecepatan tertentu lalu menabrak dengan [[CoreMechanic#^wall|wall]]
      - Perubahan arah laju secara otomatis dikalkulasi berdasarkan sudut tabrakan character dengan tembok. Misalnya, jika character menabrak tepat dari lurus depan [[CoreMechanic#^wall|wall]], maka otomatis dia akan melakukan wall rebound ke arah sebaliknya (meninggalkan tembok). Lalu, jika character menabrak [[CoreMechanic#^wall|wall]] agak lebih dari sisi kiri tembok, maka wall reboundnya akan lebih memantul ke kanan
      - Jika character melakukan wall rebound, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika wall rebound dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
      - Referensi gerakan wall rebound:
      - ![](https://youtu.be/HTI9XQ4EBNQ?si=Kd3PMzB_iD23d3oA)
  - #### Tagging
    - Character bisa melakukan tagging terhadap character lain ^tagging
    - Tagging berarti character menyemprotkan sesuatu terhadap character lawan
    - Secara default, area of effect dari semprotan tag itu seperti cone
    - Secara default, jarak semprotan tag tidak begitu jauh
    - Jika character dengan role [[CoreMechanic#^role|evader]] bertabrakan dengan semprotan tag dari character [[CoreMechanic#^role|chaser]]
    - Character [[CoreMechanic#^role|evader]] bisa dikenai tag ketika melakukan movement apa pun selama semprotan tag bertabrakan dengannya
    - Hanya character [[CoreMechanic#^role|chaser]] yang bisa melakukan aksi tagging
    - Jika character melakukan tagging, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika tagging dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character berhenti melakukan tagging

  <div id="stamina"></div>
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
    - Layout 2D ^layout-2D

    - [Cek layout The Quad dalam bentuk 2D di sini](https://www.chasealphen.nl/en/wct/)

    - ![[Asset/TheQuad2D.png]]

    - Layout 3D Interaktif ^layout-3D

    - [Cek layout The Quad dalam bentuk 3D di sini](https://sketchfab.com/3d-models/world-chase-tag-quad-98a0579a56b24a30ad83f9b7b93f0fd4)

    - ![[Asset/TheQuad3D.png]]
  - **PERHATIAN:** pada referensi sekeliling arena hanya dibatasi pagar pendek. Tapi, dalam game ini, sekeliling arena dibatasi [[CoreMechanic#^wall|wall]].
  - **PERHATIAN:** tetapi, tim development bisa memodifikasi **detail** dari layout ini.
  - ##### Batasan Modifikasi Level
    - **Modifikasi proporsi:** Tim development dipersilakan mengubah proporsi antara tiap elemen di level. Misalnya, tim development bisa memutuskan membuat bagian loading bay (cek [[CoreMechanic#^layout-2D|layout 2D]]) jadi lebih besar dibanding bagian lain berdasarkan referensi aslinya
    - **Modifikasi jenis obstacle:** Tim development dipersilakan mengubah jenis obstacle pada sebuah bagian dengan obstacle lain. Misalnya, pada bagian lazy boy (cek [[CoreMechanic#^layout-2D|layout 2D]]) tim development bisa memutuskan untuk mengubah [[CoreMechanic#^pole|pole]] pada bagian itu menjadi [[CoreMechanic#^wall|wall]].
    - **Modifikasi visual:** Tim development (khususnya tim artist) dipersilakan mengubah tampilan visual dari objek pada arena selama secara fungsi masih sama seperti fungsi pada referensi dan jenis obstacle. Misalnya, pada bagian the sisters (cek [[CoreMechanic#^layout-2D|layout 2D]]) tim artist mengubah salah satu pole menjadi secara visual tampak seperti tiang listrik.
- #### Obstacle
  - Obstacle adalah benda-benda dalam arena yang bisa diinteraksi oleh character ^obstacle
  - **PERHATIAN:** tim development bisa menggunakan beragam obstacle ini untuk memodifikasi elemen level
  - ##### Wall
    - Wall adalah tembok atau permukaan vertikal atau cukup vertikal. ^wall
    - Character bisa melakukan [[CoreMechanic#^wall-rebound|wall rebound]] jika bertabrakan dengan wall pada kecepatan tertentu
    - Character bisa melakukan [[CoreMechanic#^climb|climb]] jika wall yang dihadapi lebih tinggi daripada tinggi badan character
    - Character bisa melakukan [[CoreMechanic#^tic-tac|tic tac]] jika dia melakukan [[CoreMechanic#^jump|jump]] mengarah ke wall
  - ##### Vault box
    - Vault box adalah permukaan horizontal yang ketinggiannya setidaknya sepinggang character^vault-box
    - Character bisa melakukan [[CoreMechanic#^vault|vault]] jika dia [[CoreMechanic#^sprint|sprint]] lalu menghadapi vault box di depannya
    - Character bisa melakukan [[CoreMechanic#^jump|jump]] lalu mendarat di atas vault box
    - Character bisa melakukan [[CoreMechanic#^tic-tac|tic tac]] jika dia melakukan [[CoreMechanic#^jump|jump]] lalu berbelok ke arah lain
  - ##### Pole
    - Pole adalah tiang vertikal ^pole
    - Character bisa melakukan [[CoreMechanic#^pole-spin|pole spin]] ketika berhadapan dengan pole
  - ##### Ledge
    - Ledge adalah bagian tepi atas dari suatu [[CoreMechanic#^wall|wall]] ^ledge
    - Jika suatu [[CoreMechanic#^wall|wall]] memiliki ledge, maka character dapat melakukan [[CoreMechanic#^climb|climb]] dan menaiki ledge tersebut
  - ##### Underbar
    - Underbar adalah celah pada stuktur railing ^underbar
    - Character bisa melakukan [[CoreMechanic#^slide|slide]] ke dalam underbar dan bisa melakukan [[CoreMechanic#^vault|vault]] ke atas underbar
    - Contoh underbar dan aksi dengan underbar:
    - ![](https://youtu.be/ZKSaCLPsYj0?si=lN9UHJeUYxBI0cTR)
  - ##### Ground
    - Ground adalah segala permukaan yang bisa dipijak oleh character ^ground
    - Dia bisa berupa lantai paling bawah arena, bisa juga berupa railing dari underbar, bisa juga berupa bagian atas wall, maupun vault box.

### Decision

- Decision di sini berarti cara membuat keputusan agar character melakukan suatu aksi ^decision
- Aksi player character bisa langsung diputuskan oleh player lalu diwujudkan dengan melakukan [[CoreMechanic#^interaction|interaction]]
- Aksi AI character diputuskan dengan algoritma pengambilan keputusan yang didesain oleh tim development (programmer). **PERHATIAN:** silakan tim development melakukan riset mandiri tentang algoritma pengambilan keputusan AI dalam game dan cara implementasinya pada game engine.

### Interaction

- Interaction di sini berarti bagaimana player mewujudkan [[CoreMechanic#^decision|decision]] dalam game ini ^interaction
- Player melakukan interaction dengan menggunakan mouse dan keyboard.
- #### Camera & mouse
  - Camera dalam game adalah third-person di belakang player character
  - Rotasi camera bisa dilakukan dengan menggeser mouse
  - Camera hanya bisa melakukan pan dan tilt
    - ![[Asset/CameraMovement.png]]
  - Batasan dari rotasi camera adalah:
    - Pan: Camera bisa dirotasi sampai terlihat bagian samping 3/4 muka character. Tapi camera tidak bisa  dirotasi sampai kelihatan tampak muka character sepenuhnya dan apa-apa yang ada di belakang character
    - Tilt: Camera hanya bisa rotasi sedikit. Tidak bisa sampai melakukan tilt sehingga camera seperti ada di lantai yang menyorot ke atas. Tidak bisa juga sampai melakukan tilt sehingga atas kepala character terlihat. Paling atas camera hanya bisa melihat seperti dari balik pundak character.
  -
- #### Keyboard input
  - Player berpindah maju ke depan dengan memencet tombol W atau arah atas di keyboard
  - Player berpindah mundur ke belakang dengan memencet tombol S atau arah bawah di keyboard
  - Player melakukan strafing dengan memencet tombol A (ke kiri) atau D (ke kanan)
  - Untuk melaju belok, player harus menggunakan kombinasi tombol W dan geser mouse kiri atau kanan
  - Untuk melakukan sprint, player harus menekan tombol left shift selama beberapa lama
  - Untuk melakukan jump, player harus menekan tombol space bar
  - Untuk melakukan slide, player harus menekan mouse klik kiri saat character sedang melakukan sprint
  - Untuk melakukan vault, player harus menekan mouse klik kiri saat sedang melakukan sprint di depan vault box atau ground yang ketinggiannya setidaknya sepinggang tinggi character
  - Untuk melakukan pole spin, player harus menekan dan menahan mouse klik kiri ketika character berada di dekat pole
  - Untuk melakukan climb, player harus melakukan jump ke arah wall dan menekan mouse klik kiri
  - Untuk melakukan tic tac, player harus melakukan jump ke arah wall lalu menekan lagi space bar saat berada dekat dengan wall
  - Untuk melakukan tagging, player harus menekan mouse klik kanan
