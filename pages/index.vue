<template>
<section id="wrapper" class="container">
  <div>
    <div class="amorph-shape" id="logowrapper">
      <svg viewBox="0 0 12 18">
        <template v-for="point in letters.s.points">
          <path :key="point.id + 'a'" :id="'logo-path-'+ point.id + 'a'" class="logo-path green" :stroke-width="strokewidth" stroke="orange" stroke-linecap="round" :d=returnCoords2(point.a.y,point.a.x)></path>
          <path :key="point.id + 'b'" :id="'logo-path-'+ point.id + 'b'" class="logo-path green" :stroke-width="strokewidth" stroke="orange" stroke-linecap="round" :d=returnCoords2(point.b.y,point.b.x)></path>
        </template>
      </svg>
    </div>


  </div>
</section>
</template>

<script>
import anime from 'animejs'

export default {


  data: function() {
    return {
      // points: [
      //   [4, 0],
      //   [4, 0],
      //   [1.5, 2],
      //   [6.5, 2],
      //   [0.75, 4],
      //   [7.25, 4]
      // ],

      letters: {

        's': {
          points: [{
              'id': 0,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 0,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 0,
              },
            },
            {
              'id': 1,
              'a': {
                'visible': true,
                'x': [0.5, 2.5],
                'y': 2,
              },
              'b': {
                'visible': true,
                'x': [5.5, 7.5],
                'y': 2,
              },
            },
            {
              'id': 2,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 4,
              },
              'b': {
                'visible': true,
                'x': [6, 8],
                'y': 4,
              },
            },
            {
              'id': 3,
              'a': {
                'visible': true,
                'x': [5.2, 7.2],
                'y': 6,
              },
              'b': {
                'visible': true,
                'x': [5.2, 7.2],
                'y': 6,
              },
            },
            {
              'id': 4,
              'a': {
                'visible': true,
                'x': [0.8, 2.8],
                'y': 8,
              },
              'b': {
                'visible': true,
                'x': [0.8, 2.8],
                'y': 8,
              },
            },
            {
              'id': 5,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 10,
              },
              'b': {
                'visible': true,
                'x': [6, 8],
                'y': 10,
              },
            },
            {
              'id': 6,
              'a': {
                'visible': true,
                'x': [0.5, 2.5],
                'y': 12,
              },
              'b': {
                'visible': true,
                'x': [5.5, 7.5],
                'y': 12,
              },
            },
            {
              'id': 7,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 14,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 14,
              },
            },

          ]
        },


        't': {
          points: [{
              'id': 0,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 0,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 0,
              },
            },
            {
              'id': 1,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 2,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 2,
              },
            },
            {
              'id': 2,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 4,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 4,
              },
            },
            {
              'id': 3,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 6,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 6,
              },
            },
            {
              'id': 4,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 8,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 8,
              },
            },
            {
              'id': 5,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 10,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 10,
              },
            },
            {
              'id': 6,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 12,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 12,
              },
            },
            {
              'id': 7,
              'a': {
                'visible': true,
                'x': [0, 8],
                'y': 14,
              },
              'b': {
                'visible': true,
                'x': [0, 8],
                'y': 14,
              },
            },

          ]
        },



        'r': {
          points: [{
              'id': 0,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 0,
              },
              'b': {
                'visible': true,
                'x': [6, 8],
                'y': 0,
              },
            },
            {
              'id': 1,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 2,
              },
              'b': {
                'visible': true,
                'x': [4.8, 6.8],
                'y': 2,
              },
            },
            {
              'id': 2,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 4,
              },
              'b': {
                'visible': true,
                'x': [3.5, 5.5],
                'y': 4,
              },
            },
            {
              'id': 3,
              'a': {
                'visible': true,
                'x': [0, 4],
                'y': 6,
              },
              'b': {
                'visible': true,
                'x': [0, 4],
                'y': 6,
              },
            },
            {
              'id': 4,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 8,
              },
              'b': {
                'visible': true,
                'x': [5.5, 7.5],
                'y': 8,
              },
            },
            {
              'id': 5,
              'a': {
                'visible': true,
                'x': [6, 8],
                'y': 10,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 10,
              },
            },
            {
              'id': 6,
              'a': {
                'visible': true,
                'x': [5.5, 7.5],
                'y': 12,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 12,
              },
            },
            {
              'id': 7,
              'a': {
                'visible': true,
                'x': [0, 4],
                'y': 14,
              },
              'b': {
                'visible': true,
                'x': [0, 4],
                'y': 14,
              },
            },

          ]
        },



        'y': {
          points: [{
              'id': 0,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 0,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 0,
              },
            },
            {
              'id': 1,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 2,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 2,
              },
            },
            {
              'id': 2,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 4,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 4,
              },
            },
            {
              'id': 3,
              'a': {
                'visible': true,
                'x': [3, 5],
                'y': 6,
              },
              'b': {
                'visible': true,
                'x': [3, 5],
                'y': 6,
              },
            },
            {
              'id': 4,
              'a': {
                'visible': true,
                'x': [2, 6],
                'y': 8,
              },
              'b': {
                'visible': true,
                'x': [2, 6],
                'y': 8,
              },
            },
            {
              'id': 5,
              'a': {
                'visible': true,
                'x': [1.25, 3.25],
                'y': 10,
              },
              'b': {
                'visible': true,
                'x': [4.75, 6.75],
                'y': 10,
              },
            },
            {
              'id': 6,
              'a': {
                'visible': true,
                'x': [0.5, 2.5],
                'y': 12,
              },
              'b': {
                'visible': true,
                'x': [5.5, 7.5],
                'y': 12,
              },
            },
            {
              'id': 7,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 14,
              },
              'b': {
                'visible': true,
                'x': [6, 8],
                'y': 14,
              },
            },

          ]
        },

        'p': {
          points: [{
              'id': 0,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 0,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 0,
              },
            },
            {
              'id': 1,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 2,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 2,
              },
            },
            {
              'id': 2,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 4,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 4,
              },
            },
            {
              'id': 3,
              'a': {
                'visible': true,
                'x': [0, 4],
                'y': 6,
              },
              'b': {
                'visible': true,
                'x': [0, 4],
                'y': 6,
              },
            },
            {
              'id': 4,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 8,
              },
              'b': {
                'visible': true,
                'x': [5.5, 7.5],
                'y': 8,
              },
            },
            {
              'id': 5,
              'a': {
                'visible': true,
                'x': [6, 8],
                'y': 10,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 10,
              },
            },
            {
              'id': 6,
              'a': {
                'visible': true,
                'x': [5.5, 7.5],
                'y': 12,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 12,
              },
            },
            {
              'id': 7,
              'a': {
                'visible': true,
                'x': [0, 4],
                'y': 14,
              },
              'b': {
                'visible': true,
                'x': [0, 4],
                'y': 14,
              },
            },

          ]
        },



        'e': {
          points: [{
              'id': 0,
              'a': {
                'visible': true,
                'x': [0, 8],
                'y': 0,
              },
              'b': {
                'visible': true,
                'x': [0, 8],
                'y': 0,
              },
            },
            {
              'id': 1,
              'a': {
                'visible': true,
                'x': [0,2],
                'y': 2,
              },
              'b': {
                'visible': true,
                'x': [0,2],
                'y': 2,
              },
            },
            {
              'id': 2,
              'a': {
                'visible': true,
                'x': [0,2],
                'y': 4,
              },
              'b': {
                'visible': true,
                'x': [0,2],
                'y': 4,
              },
            },
            {
              'id': 3,
              'a': {
                'visible': true,
                'x': [0, 4],
                'y': 6,
              },
              'b': {
                'visible': true,
                'x': [0, 4],
                'y': 6,
              },
            },
            {
              'id': 4,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 8,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 8,
              },
            },
            {
              'id': 5,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 10,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 10,
              },
            },
            {
              'id': 6,
              'a': {
                'visible': true,
                'x': [0, 2],
                'y': 12,
              },
              'b': {
                'visible': true,
                'x': [0, 2],
                'y': 12,
              },
            },
            {
              'id': 7,
              'a': {
                'visible': true,
                'x': [0, 8],
                'y': 14,
              },
              'b': {
                'visible': true,
                'x': [0, 8],
                'y': 14,
              },
            },

          ]
        },



      },

      strokewidth: 0.6,
      offset: 2,
      frame: [8, 14]
    }
  },

  components: {},
  methods: {
    returnCoords: function(point) {
      return 'M' + ' ' +
        // X
        ((point[0] - this.length / 2) + this.offset) + ',' +
        // Y
        ((this.frame[1] - point[1]) + this.offset) +
        ' ' +
        // X
        ((point[0] + this.length / 2) + this.offset) + ',' +
        // Y
        ((this.frame[1] - point[1]) + this.offset)
    },

    returnCoords2: function(y, x) {
      return 'M' + ' ' +
        // X
        ((x[0]) + this.offset) + ',' +
        // Y
        ((this.frame[1] - y) + this.offset) +
        ' ' +
        // X
        ((x[1]) + this.offset) + ',' +
        // Y
        ((this.frame[1] - y) + this.offset)
    },

    animatePath(pathNumber, pathLetter) {
      if (pathLetter === 'a') {
        anime({
          targets: '#logowrapper #logo-path-' + pathNumber + pathLetter,
          d: [{
              value: this.returnCoords2(this.letters.t.points[pathNumber].a.y, this.letters.t.points[pathNumber].a.x),
            },
            {
              value: this.returnCoords2(this.letters.r.points[pathNumber].a.y, this.letters.r.points[pathNumber].a.x),
            },
            {
              value: this.returnCoords2(this.letters.y.points[pathNumber].a.y, this.letters.y.points[pathNumber].a.x),
            },
            {
              value: this.returnCoords2(this.letters.p.points[pathNumber].a.y, this.letters.p.points[pathNumber].a.x),
            },
            {
              value: this.returnCoords2(this.letters.e.points[pathNumber].a.y, this.letters.e.points[pathNumber].a.x),
            },
            {
              value: this.returnCoords2(this.letters.s.points[pathNumber].a.y, this.letters.s.points[pathNumber].a.x),
            },
          ],
          easing: 'easeInQuad',
          duration: 10000,
          loop: true,

        });
      }
      if (pathLetter === 'b') {
        anime({
          targets: '#logowrapper #logo-path-' + pathNumber + pathLetter,
          d: [{
              value: this.returnCoords2(this.letters.t.points[pathNumber].b.y, this.letters.t.points[pathNumber].b.x),
            },
            {
              value: this.returnCoords2(this.letters.r.points[pathNumber].b.y, this.letters.r.points[pathNumber].b.x),
            },
            {
              value: this.returnCoords2(this.letters.y.points[pathNumber].b.y, this.letters.y.points[pathNumber].b.x),
            },
            {
              value: this.returnCoords2(this.letters.p.points[pathNumber].b.y, this.letters.p.points[pathNumber].b.x),
            },
            {
              value: this.returnCoords2(this.letters.e.points[pathNumber].b.y, this.letters.e.points[pathNumber].b.x),
            },
            {
              value: this.returnCoords2(this.letters.s.points[pathNumber].b.y, this.letters.s.points[pathNumber].b.x),
            },
          ],
          easing: 'easeInQuad',
          duration: 10000,
          loop: true,

        });
      }
    },

    runanimejs: function() {

      this.animatePath(7, 'a')
      this.animatePath(7, 'b')

      this.animatePath(6, 'a')
      this.animatePath(6, 'b')

      this.animatePath(5, 'a')
      this.animatePath(5, 'b')

      this.animatePath(4, 'a')
      this.animatePath(4, 'b')

      this.animatePath(3, 'a')
      this.animatePath(3, 'b')

      this.animatePath(2, 'a')
      this.animatePath(2, 'b')

      this.animatePath(1, 'a')
      this.animatePath(1, 'b')

      this.animatePath(0, 'a')
      this.animatePath(0, 'b')

    },


  },
  mounted() {
    this.runanimejs()
  }
}
</script>

<style>
#logowrapper {
  position: relative;
  width: 300px;
  height: 300px;
  background:navy;
  /*margin: 0 auto;*/
  /*padding: 50px;*/
}

svg {
  /*padding: 10px;*/
}

svg {
  position: absolute;
  height: 100%;
  /*margin: 0 auto;*/
  width: 100%;
  transform:scaleX(1.1);
}

path{
  /*transform-origin: 100% 100%;*/
}

#wrapper {
  /*background: yellow;
  position: absolute;
  width: 100%;
  height: 100%;
  overflow: hidden;*/
}
</style>
