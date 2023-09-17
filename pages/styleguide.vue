<template>
  <main>
    <section>
      <div class="inner-container">
        <h1>Styleguide</h1>

        <InputField
          label="Input"
          type="text"
          v-model="input1"
        />

        <InputField
          label="Input (Disabled)"
          type="text"
          v-model="input2"
          disabled="true"
        />

        <InputTextarea
          label="Textarea"
          v-model="textarea"
        />

        <InputSelect
          label="Select"
          v-model="select"
          :options="{
            '': 'Select an option',
            'option1': 'Option 1',
            'option2': 'Option 2',
            'option3': 'Option 3'
          }"
        />

        <InputSelect
          label="Select (Disabled)"
          v-model="select2"
          :options="{
            '': 'Select an option',
            'option1': 'Option 1',
            'option2': 'Option 2',
            'option3': 'Option 3'
          }"
          disabled="true"
        />


        <InputCheckboxGroup
          title="Checkbox Group"
          :options="[{
            label: 'Option 1',
            value: 1,
          },{
            label: 'Option 2',
            value: 0
          },{
            label: 'Option 3',
            value: 2,
            disabled: true
          }]"
          selectedValues=[]
          v-model="checkbox2"
        />
        <!--
        <InputCheckbox
          title="Checkbox"
          label="Checkbox"
          v-model="checkbox1"
        />

        <InputCheckboxGroup
          title="Checkbox Group"
          :options="[{
            label: 'Yes',
            value: 1
          },{
            label: 'No',
            value: 0
          },{
            label: 'Disabled',
            value: 2,
            disabled: true
          }]"
        />
        -->

      </div>
    </section>
  </main>
</template>

<script>
  export default {
    data() {
      return {
        input1: '',
        input2: '',
        textarea: '',
        select: '',
        select2: '',
        checkbox1: '',
        checkbox2: '',
      }
    }
  }
</script>