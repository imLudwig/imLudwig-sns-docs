---
layout: page
title: Team
---

<script setup>
import {
  VPTeamPage,
  VPTeamPageTitle,
  VPTeamMembers,
  VPTeamPageSection
} from 'vitepress/theme'

const developers = [
   
        {
        avatar: 'https://avatars.githubusercontent.com/u/184827756?v=4',
        name: 'Ludwig',
        title: 'Developer',
        links: [
            { icon: 'github', link: 'https://github.com/imLudwig' },
        ]
    },
     {
        avatar: 'https://avatars.githubusercontent.com/u/147651367?v=4',
        name: 'Dusk',
        title: 'Developer',
        links: [
            { icon: 'github', link: 'https://github.com/StarBoyDusk' },
        ]
    },
     {
        avatar: 'https://avatars.githubusercontent.com/u/10331752?v=4',
        name: 'Roschy',
        title: 'Developer',
        links: [
            { icon: 'github', link: 'https://github.com/JulianLegler' },
        ]
    }
]

const specialThanks = [
    {
        avatar: 'https://avatars.githubusercontent.com/u/10902965?v=4',
        name: 'Bytesizd',
        title: 'Docs Boilerplate creator',
        links: [
            { icon: 'github', link: 'https://github.com/AndrewR3K' },
        ]
    }
]


</script>

<VPTeamPage>
  <VPTeamPageTitle>
    <template #title>Our Team</template>
    <template #lead>Meet the people who make this project happen.</template>
  </VPTeamPageTitle>

  <VPTeamPageSection>
    <template #title>Developers</template>
    <template #members>
     <VPTeamMembers size="medium" :members="developers" />
    </template>
  </VPTeamPageSection>

  <VPTeamPageSection>
    <template #title>Special Thanks</template>
    <template #members>
     <VPTeamMembers size="medium" :members="specialThanks" />
    </template>
  </VPTeamPageSection>
</VPTeamPage>
