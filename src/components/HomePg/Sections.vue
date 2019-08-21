<template>
  <div class="sections">
    <div class="sections__section">
      <p class="sections__section-heading">Echocardiography</p>
      <p class="sections__section-body">
        Supports adult, pediatric and fetal ultrasound with Z scores, chest
        wall, trans-esophageal OR TEE, ICE and stress echocardiography
        diagnostic reporting.
      </p>
    </div>
    <div class="sections__section">
      <p class="sections__section-heading">Vascular Ultrasound</p>
      <p class="sections__section-body">
        Provides a full head-to-toe vascular ultrasound reporting tool. Easy to
        use diagramming tools provide a professional touch to your reports.
      </p>
    </div>
    <div class="sections__section">
      <p class="sections__section-heading">Nuclear Stress</p>
      <p class="sections__section-body">
        Routine, nuclear exercise and pharmacologic stress and MUGA scan
        reporting. Treadmill integration makes completing stress reports fast
        and easy.
      </p>
    </div>
    <div class="sections__section">
      <p class="sections__section-heading">Cardiac Catheterization</p>
      <p class="sections__section-body">
        Cardiac and peripheral vascular diagnostic and Interventional studies.
        MD, RN, billing, inventory, PCI registry, scheduling all supported,
        Unique visual coronary tool supplants dictation.
      </p>
    </div>
    <div class="sections__section">
      <p class="sections__section-heading">Electrophysiology</p>
      <p class="sections__section-body">
        Unified system for physician, nursing, billing, inventory, ICD and AF
        registries. Ablations, devices, diagnostic studies, cardioversion and
        tilt testing supported.
      </p>
    </div>
    <div class="sections__section">
      <p class="sections__section-heading">CT/MRI</p>
      <p class="sections__section-body">
        Cardiovascular CT and MRI including coronary calcium scoring, Coronary
        and peripheral CT angiography and a full diagnostic cardiac MRI report.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sections"
};
</script>

<style lang="sass">
.sections
  display: flex
  flex-direction: row
  justify-content: center

  color: white
  border: 1px solid white

  border-radius: 20px

  margin: 0 10%

  position: absolute

  &__section
    padding: 20px

    display: flex
    flex-direction: column
    align-items: center
    justify-content: center

    text-align: center

    &-heading
      font-family: "Raleway", sans-serif
      font-weight: 700
      letter-spacing: 1px
      text-align: left

    &-body
      width: 200px
      font-size: 0.9em
      font-weight: 300
      letter-spacing: 1px
      line-height: 1.5em

      margin-top: 10px
</style>
