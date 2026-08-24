- ### Character
  - Untuk memenangkan permainan, character (baik player character maupun AI character) bisa melakukan beragam jenis movement.
  - Ketika melakukan [[CoreMechanic#^movement|movement]], character menggunakan stamina
  - Selama permainan berlangsung, character bisa mendapatkan buff & nerf dari menyentuh token buff & nerf yang dimunculkan secara sembarang di wilayah arena dalam interval tertentu
    ^movement
  - #### Movement
    - ##### Walk
  ^walk
  \- Character bisa berjalan (walk) dengan kecepatan normal
  \- Character bisa berjalan (walk) maju maupun mundur
  \- Walk tidak mengurangi stamina
  \- Jika character melakukan walk, maka [[CoreMechanic#^stamina|stamina]] bertambah seiring waktu
  \- ##### Strafing
  ^strafing
  \* Character bisa melakukan strafing (berjalan ke samping tanpa mengubah pandangan)
  \* Character bisa melakukan strafing dengan kecepatan normal
  \* Jika character melakukan strafing, maka [[CoreMechanic#^stamina|stamina]] bertambah seiring waktu
  \- ##### Sprint
  ^sprint
  \* Character bisa berlari (sprint)
  \* Berlari (sprint) berarti melaju dengan kecepatan bertambah secara bertahap
  \* Character bisa berlari (sprint) maju
  \* Jika character melakukan sprint, maka [[CoreMechanic#^stamina|stamina]] berkurang selama sprint dilakukan
  \* Character bisa melakukan sprint selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan sprint
  \- ##### Jump
  ^jump
  \- Character bisa melompat (jump)
  \- Daya lompat character dipengaruhi oleh kecepatan lajunya. Semakin cepat lajunya, semakin jauh atau tinggi lompatannya
  \- Character bisa melompat ke depan, belakang, kiri, kanan
  \- Jika character melakukan jump, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika jump dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah menjejak tanah kembali
  \- Character bisa melakukan jump selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan jump
  \- ##### Slide
  ^slide
  \- Character bisa melakukan slide
  \- Slide berarti character menjatuhkan badan dan meluncurkan tubuhnya
  \- Character bisa melakukan slide ke depan dan samping, tidak bisa ke belakang
  \- Ketika character melakukan slide, terjadi penambahan kecepatan yang lumayan drastis dalam waktu singkat, lalu melambat kembali ke kecepatan normal ketika slide berakhir
  \- Slide bisa digunakan untuk melewati [[CoreMechanic#^obstacle|obstacle]] dengan celah yang ketinggiannya lebih rendah dari pinggang character. Jadi character melakukan slide untuk masuk dan melewati celah dari [[CoreMechanic#^obstacle|obstacle]] tersebut
  \- Tetapi slide bisa juga dilakukan di mana pun
  \- Jika character melakukan slide, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika slide dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
  \- Character bisa melakukan slide selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan slide
  \- ##### Vault
  ^vault
  \- Character bisa melakukan vault
  \- Character bisa melakukan vault ke depan
  \- Vault berarti character menggunakan tangannya untuk meraih permukaan yang setidaknya lebih tinggi dari pinggangnya, lalu menarik badannya dan meluncur di atas permukaan tersebut
  \- Jika character melakukan vault, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika vault dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
  \- Character bisa melakukan vault selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan vault
  \- ##### Climb
  ^climb
  \- Character bisa memanjat (climb)
  \- Climb berarti character menggunakan tangannya untuk meraih permukaan lebih tinggi dari badan, lalu mengangkat tubuhnya sehingga bisa character menaik ke puncak permukaan tersebut
  \- Jika character melakukan climb, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika climb dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
  \- Character bisa melakukan climb selama dia memiliki [[CoreMechanic#^stamina|stamina]] yang cukup untuk melakukan climb
  \- ##### Tic tac
  ^tic-tac
  \- Character bisa melakukan tic tac
  \- Tic tac berarti character melompat mengarah ke tembok, lalu menggunakan permukaan tembok tersebut sebagai titik pijak lagi untuk melompat ke arah lain
  \- Perubahan arah lompatan ketika character melakukan tic tac secara otomatis dikalkulasi berdasarkan sudut tabrakan character dengan tembok. Misalnya, jika character menabrak tepat dari lurus depan tembok, maka otomatis dia akan melakukan tic tac ke arah sebaliknya (meninggalkan tembok). Lalu, jika character menabrak tembok agak lebih dari sisi kiri tembok, maka tic tac-nya akan lebih memantul ke kanan
  \- Jika character melakukan tic tac, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika tic tac dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah memijak tanah lagi
  \- Character bisa melakukan tic tac selama masih memiliki [[CoreMechanic#^stamina|stamina]] ketika dia melakukan [[CoreMechanic#^jump|jump]]
  \- ##### Pole spin
  ^pole-spin
  \- Character bisa melakukan pole spin
  \- Pole spin berarti character menggunakan tangannya untuk meraih vertical pole yang ada di dekatnya lalu memutarkan badannya dengan menggunakan pole tersebut sebagai poros
  \- Putaran pada pole spin bisa full (360 derajat) atau tidak full (hanya berputar sedikit, misalnya)
  \- Jika character melakukan pole spin, maka [[CoreMechanic#^stamina|stamina]] berkurang selama pole dilakukan. Jadi, [[CoreMechanic#^stamina|stamina]] bisa berkurang sedikit jika putaran tidak dilakukan sebanyak 360 derajat, misalnya.
  \- ##### Wall rebound
  ^wall-rebound
  \- Character bisa melakukan wall rebound
  \- Wall rebound berarti character melaju lalu menabrak tembok lalu mengubah arah lajunya
  \- Wall rebound dilakukan secara otomatis ketika character melaju dalam kecepatan tertentu lalu menabrak dengan tembok
  \- Perubahan arah laju secara otomatis dikalkulasi berdasarkan sudut tabrakan character dengan tembok. Misalnya, jika character menabrak tepat dari lurus depan tembok, maka otomatis dia akan melakukan wall rebound ke arah sebaliknya (meninggalkan tembok). Lalu, jika character menabrak tembok agak lebih dari sisi kiri tembok, maka wall reboundnya akan lebih memantul ke kanan
  \- Jika character melakukan wall rebound, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika wall rebound dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character sudah berdiri kembali
  - #### Tagging
  ^tagging
  \- Character bisa melakukan tagging terhadap character lain
  \- Tagging berarti character menyemprotkan sesuatu terhadap character lawan
  \- Secara default, area of effect dari semprotan tag itu seperti cone
  \- Secara default, jarak semprotan tag tidak begitu jauh
  \- Jika character dengan role [[CoreMechanic#^role|evader]] bertabrakan dengan semprotan tag dari character [[CoreMechanic#^role|chaser]]
  \- Character [[CoreMechanic#^role|evader]] bisa dikenai tag ketika melakukan movement apa pun selama semprotan tag bertabrakan dengannya
  \- Hanya character [[CoreMechanic#^role|chaser]] yang bisa melakukan aksi tagging
  \- Jika character melakukan tagging, maka [[CoreMechanic#^stamina|stamina]] berkurang sekali ketika tagging dimulai, dan [[CoreMechanic#^stamina|stamina]] baru kembali bertambah ketika character berhenti melakukan tagging
  - #### Stamina system
  ^stamina
  \- Character menggunakan stamina untuk melakukan beragam [[CoreMechanic#^movement|movement]]
  \-
  - #### Buff & Nerf
  ^buff-nerf

- ### Environment

^obstacle

- ### Struktur Permainan
  - Satu sesi permainan terdiri atas 5 [[CoreMechanic#^ronde|ronde]]
  - Sebelum sesi dimulai, dilakukan pengacakan apa [[CoreMechanic#^role|role]] dari player character maupun AI character
  - ##### Timer
  ^ronde
  \* 1 ronde dilaksanakan selama 1 menit (real-life time)

#### End condition

^end-condition

- paling lambat, permainan selesai jika sudah dilakukan 5 [[CoreMechanic#^ronde|ronde]]
- tetapi permainan bisa dinyatakan selesai jika ada satu character yang sudah memenangkan 3 [[CoreMechanic#^ronde|ronde]]
- #### Round win condition
  - Character menang di suatu ronde jika berhasil memenuhi objective dari [[CoreMechanic#^role|role]]-nya pada ronde tersebut
  - Jika menang, maka score character tersebut bertambah 1

* #### Round lose condition
  - Character kalah di suatu ronde jika gagal memenuhi objective dari [[CoreMechanic#^role|role]]-nya pada ronde tersebut

#### Role

^role

- #### Chaser

^chaser
\* Chaser adalah role di mana character harus melakukan tag pada lawan untuk memenangkan ronde
\* Character yang memiliki role chaser menang pada suatu ronde jika dia berhasil melakukan tag terhadap character lawan sebelum ronde berakhir
\* Chaser bisa melakukan [[CoreMechanic#^tagging|tagging]]

- #### Evader

^evader
\* Evader adalah role di mana character harus menghindari tag dari lawan selama ronde berlangsung
\* Character yang memiliki role evader menang pada suatu ronde jika dia berhasil tidak dikenai tag oleh character lawan sampai ronde berakhir
\* Evader tidak bisa melakukan [[CoreMechanic#^tagging|tagging]]
