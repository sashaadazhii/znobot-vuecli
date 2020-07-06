<template>
  <div>
    <div id="app">
      <div class="test-block">
        <div class="test">
          <div v-if="falseURL" class="test__question">
            <span class="question-mark">?</span>
            {{defaultContent}}
            <div class="test__heading">&gt;&gt; Варіанти відповідей:</div>
            <ul class="test__prev">
              <li class="test__prev-answer" v-for="choice in defaultChoices" :key="choice.content">
                -
                {{choice.content[1]}} {{choice.content.slice(3)}}
              </li>
            </ul>
          </div>
          <div v-else class="test__question">
            <span class="question-mark">?</span>
            {{content}}
            <div class="test__heading">&gt;&gt; Варіанти відповідей:</div>
            <ul class="test__prev">
              <li class="test__prev-answer" v-for="choice in choices" :key="choice.content">
                -
                {{choice.content[1]}} {{choice.content.slice(3)}}
              </li>
            </ul>
          </div>
        </div>
      </div>

      <div class="answer-block">
        <div class="answer" v-if="falseURL">
          <div
            class="answers-wrapper answer__item"
            v-for="answer in defaultChoices"
            :key="answer.content"
            v-bind:class="{'answer__item--true': userAnswer === answer.content && answer.is_correct, 
                          'answer__item--false': userAnswer === answer.content && !answer.is_correct}"
          >
            <label v-bind:for="answer.id" class="answer__label">
              <input
                type="radio"
                v-model="userAnswer"
                v-bind:id="answer.id"
                v-bind:value="answer.content"
                style="display:none;"
              />
              {{answer.content[1]}}
            </label>
          </div>
        </div>
        <div class="answer" v-else>
          <div
            class="answers-wrapper answer__item"
            v-for="option in choices"
            :key="option.content"
            v-bind:class="{'answer__item--true': userAnswer === option.content && option.is_correct, 
                            'answer__item--false': userAnswer === option.content && !option.is_correct}"
          >
            <label v-bind:for="option.id" class="answer__label">
              <input
                type="radio"
                v-model="userAnswer"
                v-bind:id="option.id"
                v-bind:value="option.content"
                style="display:none;"
              />
              {{option.content[1]}}
            </label>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      content: "",
      choices: [],
      userAnswer: null,
      falseURL: false,

      defaultContent: "Не мають закінчення обидва слова в рядку",
      defaultChoices: [
        { id: 0, content: "*А*: ухвалено, збудований", is_correct: false },
        { id: 1, content: "*Б*: сорок, по-полтавськи", is_correct: false },
        { id: 2, content: "*В*: горілиць, плакучі", is_correct: false },
        { id: 3, content: "*Г*: запанібрата, змито", is_correct: true }
      ]
    };
  },

  mounted() {
    var url =
      "http://zno-dev.eu-central-1.elasticbeanstalk.com/questions/random?subject=ukr";

    this.axios
      .get(url)
      .then(response => {
        this.content = response.data.content;
        this.choices = response.data.choices;
        // console.log(response.data);
      })
      .catch(error => {
        this.falseURL = true;
        console.log(error);
      });
  }
};
</script>