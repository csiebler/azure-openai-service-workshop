# Exercises

___

## :question: 01 - Simple prompt engineering

Here's an example sentence:
```
I was enjoying the sun, but then a huge cloud came and covered the sky.
```

Come up with a prompt that:

* Translates the sentence to German
* Negates the sentence
* Converts it into third person

(one prompt for each)

<details>
  <summary>:white_check_mark: See solution!</summary>

* Translates the sentence to German:
  ```
  Translate the following sentence into German.
  
  Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.
  
  German translation:
  ```

* Negates the sentence:
  ```
  Negate the following sentence.

  Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.

  Negated sentence:
  ```

* Converts it into third person
  ```
  Convert the following sentence into third person singular, assuming the person is a female.
  
  Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.

  Converted sentence:
  ```

</details>

___

## :question: 02 - Multiple tasks in one prompt

Use the same example sentence:
```
I was enjoying the sun, but then a huge cloud came and covered the sky.
```

Come up with a single prompt that:

* Translates the sentence to German
* Negates the sentence
* Converts it into third person
* And outputs the three new sentences into a JSON document

<details>
  <summary>:white_check_mark: See solution!</summary>

```
Take the following sentence and perform three tasks on it:
 
1. Translate the sentence into German
2. Negate the sentence
3. Convert it into third person, and assume the person is a female.
The output should be a JSON document. Use the keys "translated", "negated" and "third_person" in the JSON. No need to include the original text.

Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.
 
JSON:
```

</details>

___

## :question: 03 - Analyzing a customer service email

Here is a customer email:

```
Hello, my name is Mateo Gomez. I lost my Credit card on August 17th, and I would like to request its cancellation. The last purchase I made was of a Chicken parmigiana dish at Contoso Restaurant, located near the Hollywood Museum, for $40. Below is my personal information for validation:

Profession: Accountant
Social Security number is 123-45-6789
Date of birth: 9-9-1989
Phone number: 949-555-0110
Personal address: 1234 Hollywood Boulevard Los Angeles CA
Linked email account: mateo@contosorestaurant.com
Swift code: CHASUS33XXX
```

Come up with a single prompt that extract the relevant information from the email:

* Reason for contact
* Name of customer
* SSN
* Date of birth (as MM/DD/YYYY format)

Also classify the email into one of `lost_card`, `account_closure`, `address_change`. 
Give the responses as JSON.

<details>
  <summary>:white_check_mark: See solution!</summary>

```
This is an email from a customer. Extract the following information:

- Reason for contact
- Classified reason for contact (can be one of "lost_card", "account_closure", "address_change")
- Name of customer
- SSN
- Date of birth

Extract it as JSON with keys reason, classified_reason, name, ssn, dob. For dob, use MM/DD/YYYY formatting.

Email:
Hello, my name is Mateo Gomez. I lost my Credit card on August 17th, and I would like to request its cancellation. The last purchase I made was of a Chicken parmigiana dish at Contoso Restaurant, located near the Hollywood Museum, for $40. Below is my personal information for validation:
Profession: Accountant
Social Security number is 123-45-6789
Date of birth: 9-9-1989
Phone number: 949-555-0110
Personal address: 1234 Hollywood Boulevard Los Angeles CA
Linked email account: mateo@contosorestaurant.com
Swift code: CHASUS33XXX

Result:
```

</details>

___

## :question: 04 - Write a clothing description prompt

Come up with a prompt that generates a short, two sentence description for clothing articles based on metadata.

Here is some metadata:
```
Season: Winter
Style: Sweater
Gender: Female
Target group: Teenager
Material: Cotton
```

<details>
  <summary>:white_check_mark: See solution!</summary>

```
Write a two sentence tagline for this clothing article. Make it more verbose.

Season: Winter
Style: Sweater
Gender: Female
Target group: Teenager
Material: Cotton

Tagline:
```