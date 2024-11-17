<template>
  <div>
    <header>
      <h1>Our Projects</h1>
      <TabNav :tabs="['Digital Products', 'Brand Studio']" :selected="selectedTab" @selected="setSelectedTab" />
    </header>

    <main>
      <Tab :isSelected="selectedTab === 'Digital Products'">
        <DynamicContent :content="digitalProducts" />
      </Tab>
      <Tab :isSelected="selectedTab === 'Brand Studio'">
        <DynamicContent :content="brandStudio" />
      </Tab>
    </main>
  </div>
</template>

<script>
import TabNav from './components/TabNav.vue';
import Tab from './components/Tab.vue';
import DynamicContent from './components/DynamicContent.vue';

export default {
  components: { TabNav, Tab, DynamicContent },
  data() {
    return {
      selectedTab: 'Digital Products',
      digitalProducts: {
        "Banking & Finance": [
          "Kotak Netbanking",
          "Aditya Birla Capital",
          "Kotak 811",
          "Kotak CC",
          "Kotak Savings Account",
          "IDFC Save Your Tax",
          "Kotak Image Card",
          "Kotak Travel Card",
          "Kotak Insurance",
          "IDFC Saathi",
          "IDFC Dil ke Ameer"
        ],
        Fintech: ["NPCI", "Faida", "Chqbook"],
        Ecommerce: ["StayVista", "Camlin", "Asign", "Godrej", "Eureka Forbes"],
        "Education & Health": [
          "BITS Pilani",
          "ISRO",
          "Camel Wonderland",
          "Blood Buddies"
        ],
        "Real Estate": [
          "SPRE",
          "RMZ Corp",
          "ESR India",
          "The Imperial Edge",
          "SD Corp",
          "Homebuzz"
        ],
        B2B: [
          "Tata Chem",
          "Godrej",
          "Trifecta Capital",
          "Mistry Ventures",
          "White Turtle",
          "Old Bridge",
          "Shapoorji Group",
          "Symphonia",
          "Mosaic"
        ],
        "Digital Ventures": ["Fast5", "Oye Raddi"]
      },
      brandStudio: {
        "Brand Identity": [
          "Mezete",
          "Asign",
          "Aquaguard",
          "Sunrise",
          "Forbes",
          "Echo",
          "Faida",
          "Divinectar",
          "Modern History",
          "Mistry Ventures",
          "Symphonia",
          "Alsisar Hotels",
          "Old Bridge",
          "Fast5",
          "Silver Arch",
          "Oye Radio",
          "Mosaic"
        ],
        Packaging: [
          "Mezete",
          "Sunrise",
          "Divinectar",
          "Alsisar Group",
          "Modern History",
          "EurekaForbes Vacuum Cleaner"
        ],
        Campaigns: [
          "SPRE",
          "Camlin Product Ads 3D",
          "Camlin Community",
          "Camlin Open the New",
          "Stayvista",
          "Camlin Christmas",
          "Sula",
          "IDFC Dil ke Ameer",
          "Art of Play",
          "ISRO",
          "Kotak"
        ],
        "Photography & CGI": [
          "Camlin",
          "Eureka Forbes",
          "Camel",
          "SPRE",
          "BITS",
          "EFL CG"
        ],
        "Film & Videos": [
          "Camel Quality Film",
          "SPRE Minerva",
          "Camel TVC 15 Sec",
          "Wonderland 15 Sec Trailer",
          "Mosaic"
        ]
      }
    };
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    }
  }
};
</script>

<style scoped>
header {
  margin-bottom: 20px;
  text-align: center;
}

main {
  padding: 20px;
}
</style>
