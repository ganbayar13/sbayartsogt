<template>
  <div>
    <jumbotron />
    <services />
    <about />
    <what-is-new />
    <footer-section />
  </div>
</template>
<script>
import Jumbotron from '~/components/Sections/Jumbotron'
import Services from '~/components/Sections/Services'
import About from '~/components/Sections/About'
import WhatIsNew from '~/components/Sections/WhatIsNew'
import FooterSection from '~/components/Sections/FooterSection'
export default {
  components: { Jumbotron, Services, About, WhatIsNew, FooterSection }
}
</script>
