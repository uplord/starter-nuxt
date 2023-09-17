<template>
  <section>
    <div class="inner-container">
      <h1>Experiments</h1>
      <h2>Age Calculator</h2>
      <AgeCalculator/>
      <h2>Weight Convertor</h2>
      <WeightConvertor/>
      <h2>Aspect Ratio Calculator</h2>
      <AspectRatioCalculator/>
      <h2>Banner</h2>

      <BlockBanner
          id="banner"
          :slides="[{
            floating_image: 'https://placehold.co/500x500/DDD/DDD',
            title: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
            subtitle: 'Suspendisse potenti. Nunc vel tortor diam. Pellentesque habitant morbi tristique.',
            buttons: [{
              text: 'Get in touch',
              link: '/',
              class: 'large'
            }],
            class: ''
          },{
            image: 'https://placehold.co/2000x800/333/333',
            image_mobile: 'https://placehold.co/640x1000/333/333',
            title: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
            subtitle: 'Suspendisse potenti. Nunc vel tortor diam. Pellentesque habitant morbi tristique.',
            buttons: [{
              text: 'Get in touch',
              link: '/',
              class: 'large'
            }],
            class: 'text-center light'
          },{
            image: 'https://placehold.co/2000x800/EEE/EEE',
            image_mobile: 'https://placehold.co/640x1000/EEE/EEE',
            title: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
            subtitle: 'Suspendisse potenti. Nunc vel tortor diam. Pellentesque habitant morbi tristique.',
            buttons: [{
              text: 'Get in touch',
              link: '/',
              class: 'large'
            }],
            class: 'dark'
          }]"
        />
    </div>
  </section>
</template>
