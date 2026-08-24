- ### Character
  - Untuk memenangkan permainan, character (baik player character maupun AI character) bisa melakukan beragam jenis movement.
  - Ketika melakukan [[CoreMechanic#^movement|movement]], character menggunakan stamina
  - Selama permainan berlangsung, character bisa mendapatkan buff & nerf dari menyentuh token buff & nerf yang dimunculkan secara sembarang di wilayah arena dalam interval tertentu
    ^movement
  - #### Movement
    - ##### Walk
    - ##### Run
    - ##### Jump
    - ##### Slide
    - ##### Vault
    - ##### Climb
    - ##### Wall run
    - ##### Tic tac
    - ##### Ledge hanging
    - ##### Crouch
  - #### Tagging
  - #### Stamina system
  - #### Buff & Nerf

- ### Environment

- ### Struktur Permainan
  - Satu sesi permainan terdiri atas 5 ronde
  - Sebelum sesi dimulai, dilakukan pengacakan apa [[CoreMechanic#^role|role]] dari player character maupun AI character
  - ##### Timer
    - 1 ronde dilaksanakan selama 1 menit (real-life time)

#### End condition

- #### Win condition
  - Player character menang jika berhasil memenuhi objective dari [[CoreMechanic#^role|role]]-nya pada ronde tersebut

* #### Lose condition
  - Player character kalah jika gagal memenuhi objective dari [[CoreMechanic#^role|role]]-nya pada ronde tersebut

#### Role

^role

- #### Chaser
  - Chaser adalah role di mana character harus melakukan tag pada lawan untuk memenangkan ronde
- #### Evader
  - Evader adalah role di mana character harus menghindari tag dari lawan selama ronde berlangsung

#### Score
