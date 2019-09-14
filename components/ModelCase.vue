<template>
  <v-container>
    <h2>スケジュール</h2>
    <v-timeline align-top dense>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>6:30</strong>
          </v-col>
          <v-col>
            <strong>起床</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>6:45</strong>
          </v-col>
          <v-col>
            <strong>準備</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>7:15</strong>
          </v-col>
          <v-col>
            <strong>朝食</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>7:45</strong>
          </v-col>
          <v-col>
            <strong>片付け</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>8:00</strong>
          </v-col>
          <v-col>
            <strong>出勤</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>9:00</strong>
          </v-col>
          <v-col>
            <strong>仕事</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>12:00</strong>
          </v-col>
          <v-col>
            <strong>昼食</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>13:00</strong>
          </v-col>
          <v-col>
            <strong>仕事</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>18:00</strong>
          </v-col>
          <v-col>
            <strong>移動</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="teal lighten-3" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>18:30</strong>
          </v-col>
          <v-col>
            <strong>トレーニング</strong>
            <div class="caption mb-2">With</div>
            <v-avatar>
              <v-img
                src="https://avataaars.io/?avatarStyle=Circle&topType=LongHairFrida&accessoriesType=Kurt&hairColor=Red&facialHairType=BeardLight&facialHairColor=BrownDark&clotheType=GraphicShirt&clotheColor=Gray01&graphicType=Skull&eyeType=Wink&eyebrowType=RaisedExcitedNatural&mouthType=Disbelief&skinColor=Brown"
              ></v-img>
            </v-avatar>
            <v-avatar>
              <v-img
                src="https://avataaars.io/?avatarStyle=Circle&topType=ShortHairFrizzle&accessoriesType=Prescription02&hairColor=Black&facialHairType=MoustacheMagnum&facialHairColor=BrownDark&clotheType=BlazerSweater&clotheColor=Black&eyeType=Default&eyebrowType=FlatNatural&mouthType=Default&skinColor=Tanned"
              ></v-img>
            </v-avatar>
            <v-avatar>
              <v-img
                src="https://avataaars.io/?avatarStyle=Circle&topType=LongHairMiaWallace&accessoriesType=Sunglasses&hairColor=BlondeGolden&facialHairType=Blank&clotheType=BlazerSweater&eyeType=Surprised&eyebrowType=RaisedExcited&mouthType=Smile&skinColor=Pale"
              ></v-img>
            </v-avatar>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>19:30</strong>
          </v-col>
          <v-col>
            <strong>移動</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>20:00</strong>
          </v-col>
          <v-col>
            <strong>夕食</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>21:00</strong>
          </v-col>
          <v-col>
            <strong>帰宅</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>21:30</strong>
          </v-col>
          <v-col>
            <strong>風呂</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>22:00</strong>
          </v-col>
          <v-col>
            <strong>趣味</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
      <v-timeline-item color="pink" small>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>23:30</strong>
          </v-col>
          <v-col>
            <strong>就寝</strong>
          </v-col>
        </v-row>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>
<style>
.v-timeline-item__divider {
  margin-top: 16px;
}
</style>
