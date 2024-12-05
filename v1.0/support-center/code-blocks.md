---
type: page
title: Code Blocks
listed: true
slug: code-blocks
description: 
index_title: Code Blocks
hidden: 
keywords: 
tags: blocks
---

Code blocks allow you to write in pretty formatted code that has syntax highlighting in multiple coding languages.

To create a code block:

{% synced id="open-block-menu" %}
{% /synced %}

- Select Code Block {% icon classes="fas fa-code" /%}

## Supported Languages

The following languages are currently supported for syntax highlighting:

`Bash`, `C` , `C-Like`, `C++`, `C#`, `CSS`, `CSV`, `D`, `Dart`, `Django`, `Docker`, `Go`, `Groovy`, `HTML`, `HTTP`, `Javascript`, `Java`, `JSON`, `JSX`, `Kotlin`, `Lua`, `Markdown`, `Markup`, `Objective-C`, `Pascal`, `Perl`, `PHP`, `Powershell`, `Python`, `R`, `Rust`, `Ruby`, `Sass`, `Scss`, `Scala`, `SQL`, `Squirrel`, `Swift`, `Typescript`, `VB.NET`, `Visual Basic`, `XML`.

If you need more languages, we'd be happy to support them. Give us a nudge!

{% callout type="info" title="Info" %}
Syntax error highlighting only shows while editing
{% /callout %}

## Code Block Example

Here is how to write the fibonacci sequence in different languages:

{% code %}
{% tab language="javascript" %}
function fibonacci(num, memo) {
  memo = memo || {};

  if (memo[num]) return memo[num];
  if (num <= 1) return 1;

  return memo[num] = fibonacci(num - 1, memo) + fibonacci(num - 2, memo);
}
{% /tab %}
{% tab language="python" %}
# Program to display the Fibonacci sequence up to n-th term

nterms = int(input("How many terms? "))

# first two terms
n1, n2 = 0, 1
count = 0

# check if the number of terms is valid
if nterms <= 0:
   print("Please enter a positive integer")
elif nterms == 1:
   print("Fibonacci sequence upto",nterms,":")
   print(n1)
else:
   print("Fibonacci sequence:")
   while count < nterms:
       print(n1)
       nth = n1 + n2
       # update values
       n1 = n2
       n2 = nth
       count += 1
{% /tab %}
{% tab language="go" %}
func FibonacciRecursion(n int) int {
    if n <= 1 {
        return n
    }
    return FibonacciRecursion(n-1) + FibonacciRecursion(n-2)
}
{% /tab %}
{% tab language="c" %}
#include <stdio.h>
int main() {
    int i, n, t1 = 0, t2 = 1, nextTerm;
    printf("Enter the number of terms: ");
    scanf("%d", &n);
    printf("Fibonacci Series: ");
  
    for (i = 1; i <= n; ++i) {
        printf("%d, ", t1);
        nextTerm = t1 + t2;
        t1 = t2;
        t2 = nextTerm;
    }

    return 0;
}
{% /tab %}
{% tab language="ruby" %}
def fib(n)
  first_num, second_num = [0, 1]
  (n - 1).times do
    first_num, second_num = second_num, first_num + second_num
  end
  puts first_num
end
{% /tab %}
{% /code %}

## Multi Language Code Blocks

You can add multiple languages for each code block that will show as tabs, such as the example above.

## No Formatting Code Block

Code blocks can have no formatting if language "None" is selected. Also, if only language "None" was provided for the code block, then the language selector will disappear unless if the tab has a title. For example:

{% code %}
{% tab language="none" title="" %}
This is a code block with no formatting
- Correct?
{% /tab %}
{% /code %}

And another one with title:

{% code %}
{% tab language="none" title="No Formatting" %}
A titled code block without formatting keeps its title
{% /tab %}
{% /code %}

## Titled Tabs

You can also provide titles for each tab, which is a great way to identify and group the content. For example:

{% code %}
{% tab language="json" title="200 - Success" %}
[
 {
  "id": 4,
  "published": true,
  "name": "v1.0",
  "created": "2019-03-20T19:02:14+0000",
  "updated": "2019-03-20T19:02:14+0000",
  "slug": "developerhub.io-api",
  "ordr": 4
 }
]
{% /tab %}
{% tab language="json" title="403 - Access Denied" %}
{
 "error": {
  "message": "Access denied.",
  "httpCode": 403,
  "code": 403
 }
}
{% /tab %}
{% /code %}

## Collapsing Contents

Code block contents will collapse automatically (if possible) if there are more than 100 lines in the code block. All lines will be folded except the first line. Example:

{% code %}
{% tab language="yaml" %}
paths:
  /page/{id}:
    get:
      tags:
        - Page
      summary: Read page
      description: "Read a page including its content in [Darkdown](https://docs.developerhub.io/support-center/exporting-documentation#darkdown) or text format. Rate limit: 600 in 1 minute."
      operationId: read_page
      parameters:
        - name: id
          in: path
          description: Page ID
          required: true
          schema:
            type: integer
        - name: format
          in: query
          description: Format type (Default `darkdown`)
          required: false
          schema:
            type: string
            enum:
              - darkdown
              - text
      responses:
        200:
          description: OK
          headers:
            X-RateLimit-Limit:
              $ref: '#/components/headers/X-RateLimit-Limit'
            X-RateLimit-Remaining:
              $ref: '#/components/headers/X-RateLimit-Remaining'
            X-RateLimit-Reset:
              $ref: '#/components/headers/X-RateLimit-Reset'
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Page'
        403:
          description: Access denied
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/AccessDenied'
        429:
          description: Too many requests
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/TooManyRequests'
      deprecated: false
  /documentation/{id}/page:
    post:
      tags:
        - Page
      summary: Create a page
      description: "Creates a page with draft contents. To insert in a pre-existing category, set the `categoryTitle`. Rate limit: 10800 in 1 hour."
      operationId: create_page
      parameters:
        - name: id
          in: path
          description: Documentation ID
          required: true
          schema:
            type: integer
      requestBody:
        required: true
        content:
          application/json:
            schema:
              type: object
              description: Page object
              properties:
                title:
                  type: string
                  description: Title of the page
                  example: "Getting Started"
                slug:
                  type: string
                  description: Slug in the URL. Generated if it was not provided
                  example: "getting-started"
                content:
                  type: string
                  description: Draft contents of the page in [Darkdown format](https://docs.developerhub.io/support-center/exporting-documentation#darkdown)
                  example: "Let's start here\n\n##Step 1\nWelcome to **DeveloperHub**\n"
                categoryTitle:
                  type: string
                  description: To append the page to a category, provide the pre-existing category title here (case insensitive)
                  example: Installation
                message:
                  type: string
                  description: Page history message
                  default: Created using API
              required:
                - title
                - content
      responses:
        200:
          description: OK
          headers:
            X-RateLimit-Limit:
              $ref: '#/components/headers/X-RateLimit-Limit'
            X-RateLimit-Remaining:
              $ref: '#/components/headers/X-RateLimit-Remaining'
            X-RateLimit-Reset:
              $ref: '#/components/headers/X-RateLimit-Reset'
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Page'
        403:
          description: Access denied
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/AccessDenied'
        415:
          description: Unsupported content-type
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/UnsupportedContentType'
        429:
          description: Too many requests
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/TooManyRequests'
      deprecated: false
{% /tab %}
{% /code %}

You may use the widely adopted keyboard shortcuts in a code block to expand or collapse:

- Expand: {% key key="Ctrl" /%} + {% key key="I" /%}
- Collapse: {% key key="Ctrl" /%} + {% key key="Y" /%}

### Show Line Numbers

There are two ways to show line numbers:

- For each tab, you could enable showing line numbers from the tab options.
- Globally, you could enable showing line numbers for all code blocks in the project. See option `code.showLineNumbers` in [advanced settings](/support-center/advanced-settings).

## Highlight Code

Lines of code can be highlighted. From the tab option menu, you can write down the line numbers to be highlighted. The syntax for highlighting is as such:

- Use dashes `-` to make an inclusive range.
- Use commas to separate rules.

For example:

- `5-7`: Highlights lines 5 to 7.
- `1,2,3`: Highlights lines 1, 2 and 3.
- `1,10-20,25`: Highlights lines number 1, 10 to 20 and 25.

See the following code blocks for examples:

{% code %}
{% tab language="php" title="Lines 7-13" highlightLines="7-13" showLineNumbers="1" %}
/** Returns a stripped Markdown
     * @param $html
     * @return string
     */
    public static function toMarkdown($html)
    {
        $converter = new HtmlConverter();
        $converter->getConfig()->setOption('strip_tags', true);
        $converter->getConfig()->setOption('italic_style', '_');
        $converter->getConfig()->setOption('bold_style', '**');
        $converter->getConfig()->setOption('hard_break', true);

        return $converter->convert($html);
    }
{% /tab %}
{% tab language="php" title="Lines 1-6,14" highlightLines="1-6,14" showLineNumbers="1" %}
/** Returns a stripped Markdown
     * @param $html
     * @return string
     */
    public static function toMarkdown($html)
    {
        $converter = new HtmlConverter();
        $converter->getConfig()->setOption('strip_tags', true);
        $converter->getConfig()->setOption('italic_style', '_');
        $converter->getConfig()->setOption('bold_style', '**');
        $converter->getConfig()->setOption('hard_break', true);

        return $converter->convert($html);
    }
{% /tab %}
{% tab language="php" title="Lines 7,9,11,13" highlightLines="7,9,11,13" showLineNumbers="1" %}
/** Returns a stripped Markdown
     * @param $html
     * @return string
     */
    public static function toMarkdown($html)
    {
        $converter = new HtmlConverter();
        $converter->getConfig()->setOption('strip_tags', true);
        $converter->getConfig()->setOption('italic_style', '_');
        $converter->getConfig()->setOption('bold_style', '**');
        $converter->getConfig()->setOption('hard_break', true);

        return $converter->convert($html);
    }
{% /tab %}
{% /code %}