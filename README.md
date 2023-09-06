# 1213
1


    class GameScene extends Phaser.Scene {
        constructor() {
            super({ key: 'GameScene' });
        }
    
        preload() {
            console.log(preload)
            this.load.image('sky1', 'sky1.png');
            this.load.image('dune', 'dune.png'); // โหลดรูปภาพตัวละครผู้เล่น
        }
    
        create() {
            console.log(create)
            const player = this.physics.add.sprite(100, 450, 'dune'); // เปลี่ยน 'dude' เป็น 'dune'
        
            player.setBounce(0.2);
            player.setCollideWorldBounds(true);
        
            this.anims.create({
                key: 'left',
                frames: this.anims.generateFrameNumbers('dune', { start: 0, end: 3 }),
                frameRate: 10,
                repeat: -1
            });
        
            this.anims.create({
                key: 'turn',
                frames: [{ key: 'dune', frame: 4 }],
                frameRate: 20
            });
        
            this.anims.create({
                key: 'right',
                frames: this.anims.generateFrameNumbers('dune', { start: 5, end: 8 }),
                frameRate: 10,
                repeat: -1
            });
        }
    

    update() {
        onsole.log(update)
        
        // อันดับการดำเนินงานเกม
    }

}
