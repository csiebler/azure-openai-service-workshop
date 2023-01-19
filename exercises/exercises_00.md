# Exercises

## :question: Simple prompt engineering

Here's an example sentence:
> ```
> I was enjoying the sun, but then a huge cloud came and covered the sky.
> ```

Come up with a prompt that:

* Translates the sentence to German
* Negates the sentence
* Converts it into third person

(one prompt for each)

<details>
  <summary>:white_check_mark: See solution!</summary>

* Translates the sentence to German:

> ```
> Translate the following sentence into German.
> 
> Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.
> 
> German translation:
> ```

* Negates the sentence:
> ```
> Negate the following sentence.
> 
> Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.
> 
> Negated sentence:
> ```
* Converts it into third person
> ```
>Convert the following sentence into third person singular, assuming the person is a female.
>
>Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.
> 
>Converted sentence:
> ```

</details>

## :question: Multiple tasks in one prompt

Use the same example sentence:
> ```
> I was enjoying the sun, but then a huge cloud came and covered the sky.
> ```

Come up with a single prompt that:

* Translates the sentence to German
* Negates the sentence
* Converts it into third person
* And outputs the three new sentences into a JSON document

<details>
  <summary>:white_check_mark: See solution!</summary>

> ```
> Take the following sentence and perform three tasks on it:
> 
> 1. Translate the sentence into German
> 2. Negate the sentence
> 3. Convert it into third person, and assume the person is a female.
> The output should be a JSON document. Use the keys "translated", "negated" and "third_person" in the JSON. No need to include the original text.
> 
> Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.
> 
> JSON:
> ```

</details>

