# github-deploly

আজকে একটি গুরুত্বপূর্ণ বিষয় টপিক কিভাবে গিটহাবে এ্যাপ্লিকেশন ডিপ্লয় করতে হয় সে বিষয়ে আলোচন হবে -

আমরা যেকোন একটি এ্যাপ্লিকেশন ম্যানেজার ব্যবহার করতে পারি। আমি এখানে ইয়ার্ন ব্যাবহার করব । একটি এ্যাপ্লিকেশনের কাজ কমপ্লিট করার পর যখন আমারা এটি গিটহাবে রাখতে যাব তখন আমারা এই স্টেপগুলো লক্ষ্য করব। 


প্রথমে Github pages নামে একটি প্যাকেজ ইস্টল করি - 

```js
yarn add gh-pages
```
পরবর্তীতে যেভাবে গিটহাবে রিপো ওপেন করি সেভাবে রিপো ওপেন করব। এবং এ্যাপ্লিকেশেনের package.json ফাইলে কিছু কাজ করতে হবে। কাজগুলি হল - হোমপেজ এড করা, প্রিডিপ্লয়, ডিপ্লয় এগুলো নিচের দেখানোভাবে এড করা।



```js
"homepage": "https://[github username].github.io/[repo name]",

```
এই অংশের কাজগুলি script অপশনের ভিতরে রাখতে হবে।

```js
"predeploy":"yarn run build"

```

```js
"deploy":"gh-pages -d dist",
```

তারপর code push করার পর নিচের কমান্ডগুলি run করাতে হবে।

```js
yarn run build
```

```js
yarn deploy
```
একটু সময় নিবে ডিপ্লয় হতে । ডিপ্লয় কমপ্লিট হলে গিটহাবে গিয়ে চেক করতে হবে সবকিছু ঠিকঠাক আছে কিনা। যদি সবকিছু ঠিকঠাক থাকে  তাহলে  গিটহাবের **সেটিংস** অপশনে গিয়ে **পেজ** অপশনে ক্লিক করতে হবে।
একটু উপরের দিকে লক্ষ্য করলেই দেখা যাবে লাইভ লিংকটি পাবলিশ হয়ে গেছে।

# উক্ত আলোচনটি পড়ার জন্য আপনাকে ধন্যবাদ।
 Md. Muktadir Nayem
