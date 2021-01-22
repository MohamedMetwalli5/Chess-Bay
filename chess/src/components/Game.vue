<template>
  <div>
    <div id="title">
      <pre id="header" style="background-color: red color:white">
        Chess ♜♝♞♟♔♕♖♗♘♙       Turn: Player{{ (this.PlayerTurn % 2) + 1 }}
      </pre>
    </div>
    <div id="RightSide">
      <div class="grid-item" id="a8" style="background-color: white">
        <button
          class="ComputerChessPiece"
          id="ComputerR1"
          @click="from('ComputerR1')"
        ></button>
      </div>
      <div class="grid-item" id="b8" style="background-color: black">
        <button
          class="ComputerChessPiece"
          id="ComputerN1"
          @click="from('ComputerN1')"
        ></button>
      </div>

      <div class="grid-item" id="c8" style="background-color: white">
        <button
          class="ComputerChessPiece"
          id="ComputerB1"
          @click="from('ComputerB1')"
        ></button>
      </div>
      <div class="grid-item" id="d8" style="background-color: black">
        <button
          class="ComputerChessPiece"
          id="ComputerQ1"
          @click="from('ComputerQ1')"
        ></button>
      </div>

      <div class="grid-item" id="e8" style="background-color: white">
        <button
          class="ground"
          id="ComputerK1"
          @click="from('ComputerK1')"
        ></button>
      </div>
      <div class="grid-item" id="f8" style="background-color: black">
        <button
          class="ground"
          id="ComputerB2"
          @click="from('ComputerB2')"
        ></button>
      </div>
      <div class="grid-item" id="g8" style="background-color: white">
        <button
          class="ground"
          id="ComputerN2"
          @click="from('ComputerN2')"
        ></button>
      </div>
      <div class="grid-item" id="h8" style="background-color: black">
        <button
          class="ground"
          id="ComputerR2"
          @click="from('ComputerR2')"
        ></button>
      </div>

      <div class="grid-item" id="a7" style="background-color: black">
        <button
          class="ground"
          id="ComputerP1"
          @click="from('ComputerP1')"
        ></button>
      </div>
      <div class="grid-item" id="b7" style="background-color: white">
        <button
          class="ground"
          id="ComputerP2"
          @click="from('ComputerP2')"
        ></button>
      </div>
      <div class="grid-item" id="c7" style="background-color: black">
        <button
          class="ground"
          id="ComputerP3"
          @click="from('ComputerP3')"
        ></button>
      </div>
      <div class="grid-item" id="d7" style="background-color: white">
        <button
          class="ground"
          id="ComputerP4"
          @click="from('ComputerP4')"
        ></button>
      </div>

      <div class="grid-item" id="e7" style="background-color: black">
        <button
          class="ground"
          id="ComputerP5"
          @click="from('ComputerP5')"
        ></button>
      </div>
      <div class="grid-item" id="f7" style="background-color: white">
        <button
          class="ground"
          id="ComputerP6"
          @click="from('ComputerP6')"
        ></button>
      </div>

      <div class="grid-item" id="g7" style="background-color: black">
        <button
          class="ground"
          id="ComputerP7"
          @click="from('ComputerP7')"
        ></button>
      </div>
      <div class="grid-item" id="h7" style="background-color: white">
        <button
          class="ground"
          id="ComputerP8"
          @click="from('ComputerP8')"
        ></button>
      </div>
      <div class="grid-item" id="a6" style="background-color: white">
        <button class="ground" id="GroundA6" @click="from('GroundA6')"></button>
      </div>
      <div class="grid-item" id="b6" style="background-color: black">
        <button class="ground" id="GroundB6" @click="from('GroundB6')"></button>
      </div>
      <div class="grid-item" id="c6" style="background-color: white">
        <button class="ground" id="GroundC6" @click="from('GroundC6')"></button>
      </div>
      <div class="grid-item" id="d6" style="background-color: black">
        <button class="ground" id="GroundD6" @click="from('GroundD6')"></button>
      </div>

      <div class="grid-item" id="e6" style="background-color: white">
        <button class="ground" id="GroundE6" @click="from('GroundE6')"></button>
      </div>
      <div class="grid-item" id="f6" style="background-color: black">
        <button class="ground" id="GroundF6" @click="from('GroundF6')"></button>
      </div>
      <div class="grid-item" id="g6" style="background-color: white">
        <button class="ground" id="GroundG6" @click="from('GroundG6')"></button>
      </div>
      <div class="grid-item" id="h6" style="background-color: black">
        <button class="ground" id="GroundH6" @click="from('GroundH6')"></button>
      </div>
      <div class="grid-item" id="a5" style="background-color: black">
        <button class="ground" id="GroundA5" @click="from('GroundA5')"></button>
      </div>
      <div class="grid-item" id="b5" style="background-color: white">
        <button class="ground" id="GroundB5" @click="from('GroundB5')"></button>
      </div>

      <div class="grid-item" id="c5" style="background-color: black">
        <button class="ground" id="GroundC5" @click="from('GroundC5')"></button>
      </div>
      <div class="grid-item" id="d5" style="background-color: white">
        <button class="ground" id="GroundD5" @click="from('GroundD5')"></button>
      </div>
      <div class="grid-item" id="e5" style="background-color: black">
        <button class="ground" id="GroundE5" @click="from('GroundE5')"></button>
      </div>
      <div class="grid-item" id="f5" style="background-color: white">
        <button class="ground" id="GroundF5" @click="from('GroundF5')"></button>
      </div>
      <div class="grid-item" id="g5" style="background-color: black">
        <button class="ground" id="GroundG5" @click="from('GroundG5')"></button>
      </div>
      <div class="grid-item" id="h5" style="background-color: white">
        <button class="ground" id="GroundH5" @click="from('GroundH5')"></button>
      </div>

      <div class="grid-item" id="a4" style="background-color: white">
        <button class="ground" id="GroundA4" @click="from('GroundA4')"></button>
      </div>
      <div class="grid-item" id="b4" style="background-color: black">
        <button class="ground" id="GroundB4" @click="from('GroundB4')"></button>
      </div>

      <div class="grid-item" id="c4" style="background-color: white">
        <button class="ground" id="GroundC4" @click="from('GroundC4')"></button>
      </div>
      <div class="grid-item" id="d4" style="background-color: black">
        <button class="ground" id="GroundD4" @click="from('GroundD4')"></button>
      </div>
      <div class="grid-item" id="e4" style="background-color: white">
        <button class="ground" id="GroundE4" @click="from('GroundE4')"></button>
      </div>
      <div class="grid-item" id="f4" style="background-color: black">
        <button class="ground" id="GroundF4" @click="from('GroundF4')"></button>
      </div>

      <div class="grid-item" id="g4" style="background-color: white">
        <button class="ground" id="GroundG4" @click="from('GroundG4')"></button>
      </div>
      <div class="grid-item" id="h4" style="background-color: black">
        <button class="ground" id="GroundH4" @click="from('GroundH4')"></button>
      </div>
      <div class="grid-item" id="a3" style="background-color: black">
        <button class="ground" id="GroundA3" @click="from('GroundA3')"></button>
      </div>
      <div class="grid-item" id="b3" style="background-color: white">
        <button class="ground" id="GroundB3" @click="from('GroundB3')"></button>
      </div>

      <div class="grid-item" id="c3" style="background-color: black">
        <button class="ground" id="GroundC3" @click="from('GroundC3')"></button>
      </div>
      <div class="grid-item" id="d3" style="background-color: white">
        <button class="ground" id="GroundD3" @click="from('GroundD3')"></button>
      </div>

      <div class="grid-item" id="e3" style="background-color: black">
        <button class="ground" id="GroundE3" @click="from('GroundE3')"></button>
      </div>
      <div class="grid-item" id="f3" style="background-color: white">
        <button class="ground" id="GroundF3" @click="from('GroundF3')"></button>
      </div>
      <div class="grid-item" id="g3" style="background-color: black">
        <button class="ground" id="GroundG3" @click="from('GroundG3')"></button>
      </div>
      <div class="grid-item" id="h3" style="background-color: white">
        <button class="ground" id="GroundH3" @click="from('GroundH3')"></button>
      </div>
      <div class="grid-item" id="a2" style="background-color: white">
        <button class="ground" id="p8" @click="from('p8')"></button>
      </div>
      <div class="grid-item" style="background-color: black">
        <button class="ground" id="p7" @click="from('p7')"></button>
      </div>

      <div class="grid-item" id="c2" style="background-color: white">
        <button class="PlayerChessPiece" id="p6" @click="from('p6')"></button>
      </div>
      <div class="grid-item" id="d2" style="background-color: black">
        <button class="PlayerChessPiece" id="p5" @click="from('p5')"></button>
      </div>
      <div class="grid-item" id="e2" style="background-color: white">
        <button class="PlayerChessPiece" id="p4" @click="from('p4')"></button>
      </div>
      <div class="grid-item" id="f2" style="background-color: black">
        <button class="PlayerChessPiece" id="p3" @click="from('p3')"></button>
      </div>
      <div class="grid-item" id="g2" style="background-color: white">
        <button class="PlayerChessPiece" id="p2" @click="from('p2')"></button>
      </div>
      <div class="grid-item" id="h2" style="background-color: black">
        <button class="PlayerChessPiece" id="p1" @click="from('p1')"></button>
      </div>

      <div class="grid-item" id="a1" style="background-color: black">
        <button class="PlayerChessPiece" id="r2" @click="from('r2')"></button>
      </div>
      <div class="grid-item" style="background-color: white">
        <button class="PlayerChessPiece" id="n2" @click="from('n2')"></button>
      </div>
      <div class="grid-item" id="c1" style="background-color: black">
        <button class="PlayerChessPiece" id="b2" @click="from('b2')"></button>
      </div>
      <div class="grid-item" id="d1" style="background-color: white">
        <button class="PlayerChessPiece" id="q1" @click="from('q1')"></button>
      </div>
      <div class="grid-item" id="e1" style="background-color: black">
        <button class="PlayerChessPiece" id="k1" @click="from('k1')"></button>
      </div>
      <div class="grid-item" id="f1" style="background-color: white">
        <button class="PlayerChessPiece" id="b1" @click="from('b1')"></button>
      </div>

      <div class="grid-item" id="g1" style="background-color: black">
        <button class="PlayerChessPiece" id="n1" @click="from('n1')"></button>
      </div>
      <div class="grid-item" id="h1" style="background-color: white">
        <button class="PlayerChessPiece" id="r1" @click="from('r1')"></button>
      </div>
    </div>
    <div>
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499806</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499803</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499812 </pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499811</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499814</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499813</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499801</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499800</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499808</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499807</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499810</pre
      >
      <pre style="font-size: 4px">
https://commons.wikimedia.org/w/index.php?curid=1499809</pre
      >
      <pre style="font-size: 4px">
The chessPieces vectors images were created , By en:User:Cburnett.  CC BY-SA 3.0 </pre
      >
    </div>
  </div>
</template>
<script>
export default {
  name: "Game",
  data: function () {
    return {
      PlayerTurn: 0,
      ClickCounter: 0,
      FromElementID: "",
      ToElementID: "",
      whiteQueenLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Chess_qlt45.svg/1024px-Chess_qlt45.svg.png",
      blackQueenLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/Chess_qdt45.svg/1024px-Chess_qdt45.svg.png",
      whiteKingLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/4/42/Chess_klt45.svg/1024px-Chess_klt45.svg.png",
      blackKingLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/f/f0/Chess_kdt45.svg/1024px-Chess_kdt45.svg.png",
      whiteBishopLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/Chess_blt45.svg/1024px-Chess_blt45.svg.png",
      blackBishopLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/9/98/Chess_bdt45.svg/1024px-Chess_bdt45.svg.png",
      whitePawnLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Chess_plt45.svg/1024px-Chess_plt45.svg.png",
      blackPawnLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/c/c7/Chess_pdt45.svg/1024px-Chess_pdt45.svg.png",
      whiteRockLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/7/72/Chess_rlt45.svg/1024px-Chess_rlt45.svg.png",
      blackRockLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/f/ff/Chess_rdt45.svg/1024px-Chess_rdt45.svg.png",
      whiteKnightLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/7/70/Chess_nlt45.svg/1024px-Chess_nlt45.svg.png",
      blackKnightLink:
        "https://upload.wikimedia.org/wikipedia/commons/thumb/e/ef/Chess_ndt45.svg/1024px-Chess_ndt45.svg.png",
      WhitePieces: [
        "https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Chess_qlt45.svg/1024px-Chess_qlt45.svg.png",
        "https://upload.wikimedia.org/wikipedia/commons/thumb/4/42/Chess_klt45.svg/1024px-Chess_klt45.svg.png",
        "https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/Chess_blt45.svg/1024px-Chess_blt45.svg.png",
        "https://upload.wikimedia.org/wikipedia/commons/thumb/7/70/Chess_nlt45.svg/1024px-Chess_nlt45.svg.png",
        "https://upload.wikimedia.org/wikipedia/commons/thumb/7/72/Chess_rlt45.svg/1024px-Chess_rlt45.svg.png",
        "https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Chess_plt45.svg/1024px-Chess_plt45.svg.png",
      ],
      FlippedPieces: [
        "ComputerR1",
        "r2",
        "ComputerR2",
        "r1",
        "ComputerN2",
        "n1",
        "ComputerN1",
        "n2",
        "ComputerQ1",
        "q1",
        "ComputerK1",
        "k1",
        "ComputerB2",
        "b1",
        "ComputerB1",
        "b2",
        "ComputerP8",
        "p1",
        "ComputerP7",
        "p2",
        "ComputerP6",
        "p3",
        "ComputerP5",
        "p4",
        "ComputerP4",
        "p5",
        "ComputerP3",
        "p6",
        "ComputerP2",
        "p7",
        "ComputerP1",
        "p8",
        "GroundA3",
        "GroundB3",
        "GroundC3",
        "GroundD3",
        "GroundE3",
        "GroundF3",
        "GroundG3",
        "GroundH3",
        "GroundA4",
        "GroundB4",
        "GroundC4",
        "GroundD4",
        "GroundE4",
        "GroundF4",
        "GroundG4",
        "GroundH4",
        "GroundA5",
        "GroundB5",
        "GroundC5",
        "GroundD5",
        "GroundE5",
        "GroundF5",
        "GroundG5",
        "GroundH5",
        "GroundA6",
        "GroundB6",
        "GroundC6",
        "GroundD6",
        "GroundE6",
        "GroundF6",
        "GroundG6",
        "GroundH6",
      ],
    };
  },
  methods: {
    from(index) {
      if (this.ClickCounter % 2 === 0) {
        this.FromElementID = index;
        console.log(
          this.FromElementID + "  at clickCounter :  " + this.ClickCounter
        );
        this.ClickCounter++;
      } else {
        this.ToElementID = index;
        console.log(
          this.ToElementID + "  at clickCounter :  " + this.ClickCounter
        );
        this.ClickCounter++;
        this.NextMoveFunc();
        // this.PlayerTurn++;
      }
    },

    NextMoveFunc() {
      if (
        this.FromElementID &&
        this.ToElementID &&
        this.ClickCounter % 2 === 0 &&
        this.ClickCounter > 0
      ) {
        //this.Flipper();
        var temp = document.getElementById(this.FromElementID),
          styleTemp = temp.currentStyle || window.getComputedStyle(temp, false),
          checker = styleTemp.backgroundImage.slice(4, -1).replace(/"/g, "");
        let FromColor = "",
          ToColor = "";
        for (let i = 0; i < this.WhitePieces.length; i++) {
          if (
            this.WhitePieces[i]
              .normalize()
              .localeCompare(checker.normalize()) === 0
          ) {
            FromColor = "white";
            console.log("it is white");
            break;
          }
          if (i + 1 === this.WhitePieces.length) {
            FromColor = "black";
            console.log("it is black");
          }
        }

        var temp2 = document.getElementById(this.ToElementID),
          styleTemp2 =
            temp.currentStyle || window.getComputedStyle(temp2, false),
          checker2 = styleTemp2.backgroundImage.slice(4, -1).replace(/"/g, "");
        for (let i = 0; i < this.WhitePieces.length; i++) {
          if (
            this.WhitePieces[i]
              .normalize()
              .localeCompare(checker2.normalize()) === 0
          ) {
            ToColor = "white";
            console.log("it is white");
            break;
          }
          if (i + 1 === this.WhitePieces.length) {
            ToColor = "black";
            console.log("it is black");
          }
        }
        //temp = checker;
        //checker2 = temp;
        if (
          (FromColor !== ToColor && checker.length !== 0) ||
          (checker2.length === 0 && checker.length !== 0)
        ) {
          this.Rotater();
          this.PlayerTurn++;
          //alert(this.FromElementID + " --> " + this.ToElementID);
          var img = document.getElementById(this.FromElementID),
            style = img.currentStyle || window.getComputedStyle(img, false),
            bi = style.backgroundImage.slice(4, -1).replace(/"/g, "");

          document.getElementById(this.FromElementID).style.backgroundImage =
            "none";
          document.getElementById(this.ToElementID).style.backgroundImage =
            "url(" + bi + ")";

          document.getElementById(this.ToElementID).style.display = "block";
          document.getElementById(this.ToElementID).style.backgroundSize =
            "50%";
          document.getElementById(this.ToElementID).style.backgroundPosition =
            "center";
          document.getElementById(this.ToElementID).style.backgroundRepeat =
            "no-repeat";
        }
      }
    },
    Rotater() {
      if (this.PlayerTurn % 2 !== 0) {
        document
          .getElementById("RightSide")
          .style.setProperty("-webkit-transform", "scaleY(1)", null);
        for (let i = 0; i < this.FlippedPieces.length; i++) {
          document
            .getElementById(this.FlippedPieces[i])
            .style.setProperty("-webkit-transform", "scaleY(1)", null);
        }
      } else {
        document
          .getElementById("RightSide")
          .style.setProperty("-webkit-transform", "scaleY(-1)", null);
        for (let i = 0; i < this.FlippedPieces.length; i++) {
          document
            .getElementById(this.FlippedPieces[i])
            .style.setProperty("-webkit-transform", "scaleY(-1)", null);
        }
      }
    },
  },
};
</script>
<style  scoped>
#RightSide {
  margin: 0.5px;
  float: center;
  width: 100%;
  display: grid;
  grid-template-columns: auto auto auto auto auto auto auto auto;
  background-color: #000000;
  padding: 0.25%;
}

.grid-item {
  border: 1px solid rgba(0, 0, 0, 0.8);
  padding: 1%;
  font-size: 30px;
  border-radius: 5px;
  text-align: center;
}

.PlayerPiece {
  border: solid;
  border-radius: 5px;
  height: 60px;
}

.PlayerChessPiece {
  margin: auto;
  width: 145px;
  height: 70px;
  background: rgb(255, 255, 255);
  border-radius: 20px;
  font-size: 30px;
}

.ComputerChessPiece {
  margin: auto;
  width: 145px;
  height: 70px;
  background: rgb(255, 255, 255);
  border-radius: 20px;
  font-size: 30px;
}

.ground {
  margin: auto;
  width: 145px;
  height: 70px;
  border-radius: 20px;
  background: rgb(255, 255, 255);
  font-size: 30px;
}

#r1,
#r2 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/7/72/Chess_rlt45.svg/1024px-Chess_rlt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#k1 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/4/42/Chess_klt45.svg/1024px-Chess_klt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#q1 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Chess_qlt45.svg/1024px-Chess_qlt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#b1,
#b2 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/Chess_blt45.svg/1024px-Chess_blt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#n1,
#n2 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/7/70/Chess_nlt45.svg/1024px-Chess_nlt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#p1,
#p2,
#p3,
#p4,
#p5,
#p6,
#p7,
#p8 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Chess_plt45.svg/1024px-Chess_plt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}
#ComputerR1,
#ComputerR2 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/f/ff/Chess_rdt45.svg/1024px-Chess_rdt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#ComputerN1,
#ComputerN2 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/e/ef/Chess_ndt45.svg/1024px-Chess_ndt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#ComputerB1,
#ComputerB2 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/9/98/Chess_bdt45.svg/1024px-Chess_bdt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#ComputerQ1 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/Chess_qdt45.svg/1024px-Chess_qdt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#ComputerK1 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/f/f0/Chess_kdt45.svg/1024px-Chess_kdt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#ComputerP1,
#ComputerP2,
#ComputerP3,
#ComputerP4,
#ComputerP5,
#ComputerP6,
#ComputerP7,
#ComputerP8 {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/c/c7/Chess_pdt45.svg/1024px-Chess_pdt45.svg.png");
  background-size: 55%;
  background-position: center;
  background-repeat: no-repeat;
}

#title {
  height: 70px;
  width: 100%;
  margin-top: -16px;
  /* background-image: url("../assets/BackGround.png"); */
  background-size: 70px;
  background-position: center;
  background-repeat: no-repeat;
  border: solid;
  border-radius: 20px;
  border-color: red;
  background-color: red;
}

#header {
  margin-top: 10px;
  background-color: red;
  color: white;
  font-size: 40px;
}
</style>