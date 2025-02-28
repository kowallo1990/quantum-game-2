<template>
  <g :style="positionStyle" @mouseenter="handleMouseEnter" @mouseleave="handleMouseLeave">
    <rect :width="tileSize" :height="tileSize" />
    <component
      :is="cell.element.name"
      :cell="cell"
      :class="cell.element.name"
      :cell-size="tileSize"
      :border="border"
    />
  </g>
</template>

<script lang="ts">
import { Component, Emit, Vue, Prop } from 'vue-property-decorator';
import { Cell } from 'quantumweasel';
import {
  Laser,
  Mirror,
  BeamSplitter,
  PolarizingBeamSplitter,
  CoatedBeamSplitter,
  CornerCube,
  Detector,
  Rock,
  Mine,
  Absorber,
  DetectorFour,
  Polarizer,
  QuarterWavePlate,
  SugarSolution,
  FaradayRotator,
  Glass,
  VacuumJar
} from './pieces';

const borderColors = {
  active: '#FF0055',
  rotable: 'yellow',
  energized: 'blue'
};

@Component({
  components: {
    Laser,
    Mirror,
    BeamSplitter,
    PolarizingBeamSplitter,
    CoatedBeamSplitter,
    CornerCube,
    Detector,
    Rock,
    Mine,
    Absorber,
    DetectorFour,
    Polarizer,
    QuarterWavePlate,
    SugarSolution,
    FaradayRotator,
    Glass,
    VacuumJar
  }
})
export default class QCell extends Vue {
  @Prop() readonly cell!: Cell;
  @Prop() readonly lasers!: any[];
  @Prop({ default: false}) readonly tool!: boolean;
  @Prop() readonly tileSize!: number;

  border = '';

  get positionStyle() {
    let styleObj = {};
    const originX = this.centerCoord(this.cell.coord.x);
    const originY = this.centerCoord(this.cell.coord.y);
    if (this.cell.element.name !== 'Void' && !this.tool) {
      styleObj = {
        'transform-origin': `${originX}px ${originY}px`,
        transform: `
				rotate(-${this.cell.rotation}deg)
				translate(${this.cell.coord.x * this.tileSize}px, ${this.cell.coord.y * this.tileSize}px)`
      };
    }
    return styleObj;
  }

  centerCoord(val: number) {
    return (val + 0.5) * this.tileSize;
  }

  handleMouseEnter() {
    this.border = borderColors.rotable;
  }

  handleMouseLeave() {
    this.border = '';
  }

  get translationX(): number {
    return this.cell.coord.x * this.tileSize;
  }

  get translationY(): number {
    return this.cell.coord.y * this.tileSize;
  }
}
</script>

<style lang="scss">
rect {
  fill: transparent;
}
</style>
