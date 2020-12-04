---
layout: archive
lang: en
ref: test
read_time: true
share: true
author_profile: false
permalink: /docs/en/platform/turtlebot3/quick-start/
tabs: "ROS"
tab_title1: Kinetic
tab_title2: Melodic
tab_title3: Noetic
sidebar:
  title: TurtleBot3
  nav: "test"
product_group: test
page_number: 6
---

<div style="counter-reset: h1 1"></div>
<div style="counter-reset: h2 1"></div>

{::options parse_block_html="true" /}

<section id="{{ page.tab_title1 }}" class="tab_contents">

{% include en/platform/test/kinetic_quickstart.md %}

</section>

<section id="{{ page.tab_title2 }}" class="tab_contents">
{% include en/platform/test/melodic_quickstart.md %}

</section>

<section id="{{ page.tab_title3 }}" class="tab_contents">
{% include en/platform/test/noetic_quickstart.md %}

</section>

<!--

Log:
20201018
- JS code is addeds to default.html.
- The made js code performs adding a class named "selected" to .archive class.
- when archive class name is changed, I want the include specific fragnments will appear and the other fragments not show up (display: none;)

20201019
- If statement only works one time when the pate is loaded. Manipulate css property, display: none or block.

20201020
- {::options parse_block_html="true" /} 옵션을 통해, Block Level 의 블럭과 마크다운을 같이 사용할수있다.
- {: .} 로 통해, ID 또는 class 지정이 가능하다.

20201029

- Page 로드시, Object에 data를 저장하여 Tab이 게속 선택되어지게끔 해야한다.
- tutorialrepublic.com/faq/how-to-keep-the-current-tab-active-on-page-reload-in-bootstrap.php#:~:text=Answer%3A%20Use%20the%20HTML5%20localStorage,tab%20selected%20on%20page%20reload.

-->
