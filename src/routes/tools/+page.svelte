<script lang="ts">
  import type { Tool } from '$lib/models/tools';
  import ToolCard from '$lib/components/tools/ToolCard.svelte';
  import MetaDescriptors from '$lib/components/utils/MetaDescriptors.svelte';

  // cspell:ignore SatisGraphtory tehalexf thinkaliker Moritz
  const tools: Tool[] = [
    {
      name: 'Satisfactory Calculator Interactive Map (SCIM)',
      author: 'Anthor',
      logo: 'https://i.imgur.com/vPKmL9d.png',
      description:
        'Collection of tools for Satisfactory - Production planner, Interactive map/save editor, Recipes, etc. (Supports 1.0 Release save files.)',
      link: 'https://satisfactory-calculator.com/'
    },
    {
      name: 'Satisfactory Tools',
      author: 'greeny',
      logo: 'https://i.imgur.com/WQEHo26.png',
      description:
        'A collection of powerful tools for planning and building the perfect base. Calculate your production or consumption, browse items, buildings, and schematics and share your builds with others!',
      link: 'https://www.satisfactorytools.com/'
    },
    {
      name: 'FactorioLab',
      author: 'Doug Broad',
      logo: 'https://factoriolab.github.io/factoriolab.webp',
      description: 'Production calculator supporting multiple factory games and visualization approaches.',
      link: 'https://factoriolab.github.io/satisfactory'
    },
    {
      name: 'Satisfactory Save File Python Tools',
      author: 'GreyHak',
      logo: 'https://raw.githubusercontent.com/GreyHak/sat_sav_parse/main/sat_py_icon.png',
      description:
        'A set of Python tools for parsing Satisfactory save files, and then displaying and manipulating the contents. (Supports 1.0 Release save files.)',
      link: 'https://github.com/GreyHak/sat_sav_parse'
    },
    {
      name: 'Recipe Calculator',
      author: 'KirkMcDonald',
      logo: '',
      description: 'Recipe calculator using sankey diagrams.',
      link: 'https://kirkmcdonald.github.io/satisfactory-calculator/calc.html'
    },
    {
      name: 'Satisfactory 3D Map',
      author: 'Moritz',
      logo: '',
      description:
        'Shows all objects within a savegame in 3D and provides a simple version of the game world for spatial context. Additionally, all properties and values of objects are shown.',
      link: 'https://github.com/moritz-h/satisfactory-3d-map'
    },
    {
      name: 'Satisfactory Dedicated Server Remote Manager',
      author: 'GreyHak',
      logo: 'https://raw.githubusercontent.com/GreyHak/sdsrm/main/sdsrm_icon.png',
      description:
        'Manage your 1.0+ Dedicated Server remotely with this Python GUI through the new Dedicated Server HTTPS API.  If you want a make your own remote manager, a Python library is available.',
      link: 'https://github.com/GreyHak/sdsrm'
    },
    {
      name: 'Satisfactory Logistics',
      author: 'leonardfactory',
      logo: 'https://satisfactory-logistics.xyz/images/logo/logo-square-big.png',
      description:
        'Keep track of in-game Logistics (by train, drones, vehicles), setup inputs and outputs between them and see how many items are consumed and where.',
      link: 'https://satisfactory-logistics.xyz/'
    },
    {
      name: 'Satisfactory UI Kit',
      author: 'Deantendo',
      logo: '',
      description: 'A UI kit for developing Satisfactory mods.',
      link: 'https://github.com/deantendo/sfuikit'
    },
    {
      name: "Daniel's Satisfactory Tools",
      author: 'DanielTheProgrammer',
      logo: 'https://i.imgur.com/Ogt0r9k.png',
      description: 'Visualize production chains, and browse items and recipes! (Pre-1.0 release recipes)',
      link: 'https://daniel2013.github.io/satisfactory/'
    },
    {
      name: 'Save Editor',
      author: 'Goz3rr',
      logo: 'https://cdn.jsdelivr.net/gh/Goz3rr/SatisfactorySaveEditor@6958101e3f2c0e50ba92df798ebefe4e6bdd4eb5/Reference%20Materials/SatisfactorySaveEditorLogo.png',
      description:
        'A work in progress save editor for Satisfactory. Consists of both a save parser and an application for viewing and editing the parsed data. (Supports Update 5 save files.)',
      link: 'https://github.com/Goz3rr/SatisfactorySaveEditor'
    },
    {
      name: 'SatisGraphtory',
      author: 'tehalexf and thinkaliker',
      logo: 'https://cdn.jsdelivr.net/gh/rhocode/rhocode.github.io@4713b4887e8821f1482de7af4ae32fb6a4b2bcaf/img/satoolsfactory_icons/dot.png',
      description:
        'This is a factory planner/optimizer/analyzer tool for factories old and new! Simulate resource chains, factory layouts, and more! (pre-Update 4 recipes)',
      link: 'https://satisgraphtory.com/'
    }
  ];
</script>

<svelte:head>
  <title>Tools - SMR</title>
  <MetaDescriptors
    description="A collection of useful tools for Satisfactory, such as recipe calculators and save editors"
    title="Tools" />
</svelte:head>

<h1 class="my-4 text-4xl font-bold">Tools</h1>
<div class="grid grid-cols-1 gap-4 2xl:grid-cols-2 3xl:grid-cols-3">
  {#each tools as tool}
    <ToolCard {tool} />
  {/each}
</div>
