# Interactive Blocks

In addition to the default Markdown you can write, GitBook has a number of out-of-the-box interactive blocks you can use. You can find interactive blocks by pressing `/` to see which ones you can use.

<figure><img src="https://gitbookio.github.io/onboarding-template-images/interactive-hero.png" alt=""><figcaption></figcaption></figure>

### Tabs

{% tabs %}
{% tab title="First Tab" %}
Each tab is like a mini page — it can contain multiple other blocks, of any type. So you can add code blocks, images, integration blocks and more to individual tabs in the same tab block.
{% endtab %}

{% tab title="Second Tab" %}
Add images, embedded content, and code blocks, and more.

```javascript
const handleFetchEvent = async (request, context) => {
    return new Response({message: "Hello World"});
};
```
{% endtab %}
{% endtabs %}

### Expandable Sections

<details>

<summary>Click me to expand</summary>

Expandable blocks are helpful in condensing what could otherwise be a lengthy paragraph. They are also great in step-by-step guides and FAQs.

</details>

### Drawings

<img alt="" class="gitbook-drawing">

### Embedded Content

{% embed url="https://www.youtube.com/watch?v=YILlrDYzAm4" %}

{% hint style="info" %}
GitBook supports thousands of embedded websites out of the box, simply by pasting their links. Feel free to check out which ones are supported natively [here](https://iframely.com/).
{% endhint %}
