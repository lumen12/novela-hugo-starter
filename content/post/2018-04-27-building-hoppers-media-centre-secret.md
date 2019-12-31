---
title: A story of why Forestry loves Hugo
date: 2017-04-27
hero: "/images/hero-3.jpg"
excerpt: Creating a new website for Hopper, one of the top 4 most downloaded travel
  apps in the U.S, along with Uber, Lyft.
secret: true
timeToRead: 8
authors: []

---
피그 마가 회사를 위해 최고의 디자인 툴인 이유를 이해했습니다. 저는 디자이너로서 호퍼, 라이트 스피드 및 브리더와 같은 회사의 성장에 기여했습니다. 전 세계 스타트 업 그레 이드 할 수 있습니다. 우리는이 팀을 내러티브라고 부하십시오.

내레이션은 전 세계 3 개 도시에 스튜디오 스튜디오입니다. 우리는 이미 도전에 도전하고 있습니다. 지리학.

우리는 첫 번째 프로젝트에 참여했습니다. 내레이션을하기 전에 몇 년 동안 스케치를 할 수있게되었습니다.

새로운 도구를 다시 배우자 운 좋게도 전환은 자연스럽지 않다. Figma에 대한 작업은 제 2의 성격을 지니고있다. 3 주 만에 나는 팬이면서도 아마 아마 옹호자 일 것입니다. 여기에 8 가지 이유가 있습니다.

## 쉬운 운명

아직 정말 많지 않았다. 말 그대로 아트 보드입니다. 그렇게해야합니다. 이 플랫폼은 매우 용서하고 전환을 준비합니다.

## 제로 파일 관리

그게 무슨 뜻이야? 스케치, 프레이머, Adobe XD 또는 Photoshop은 작업을 저장해야합니다. 기본 앱입니다. 물론 다양한 도구를 사용할 수 있습니다. 그리고 네, 디스크를 잃어 버렸거나, 컴퓨터를 쓸 수 있습니다.

Figma가 아닙니다. command + s를 수행 할 필요가 있습니다. Figma는 웹 기반 소프트웨어 성능 버전을 다시 업로드 할 수 있습니다. 구글 문서 도구를 상상할 수 있습니다. 디자인 파일을위한 유일한 소스.

필자는 프로젝트를 30GB 이상으로 확장했습니다.

## 피그 마는 플랫폼에 구애받지

웹 기반 소프트웨어의 가장 좋은 기능 중 하나는 더 이상 운영 할 수 있습니다. 기본 나 래퍼입니다. 홈 오피스의 iMac Pro에서 Surface Book 2를 계속 진행할 수 있습니다. 대단합니다.

추가로 고통스러운 소프트웨어 업데이트를 다운로드 할 수 있습니다. "클라우드"는 2018 년입니다.

## 공연

웹에서 본격적인 디자인 앱을 제공합니다. 나는 똑같이 생각한다.

나는 항상 스케치를한다. 그래 피그입니다.

나는“웹 페이지”를 시작했다. 구성 요소 및 스타일과 제품 디자인 도구가 제공됩니다.

At Narative, as we constantly change projects, styles and teams, one of the best ways for us to keep in sync is by publishing components. Even in different projects, or “files”, we can load components and libraries from previous projects, allowing us to be extremely efficient and consistent.

Building components such as buttons, modals, and form fields is awesome. Say you build 30 pages using one single library of components, and if you ever decide to update the style of a button from this library, for example, you simply update the master and, voilà — all 30 pages will have the brand new and updated button.

## Our engineers love it

From an engineering perspective, it’s extremely efficient having our projects centralized in one platform. In the past, every time I updated a project, I had to manually sync my designs through a plugin into a third-party “inspection” platform where engineers would have access to. Although this method works, it’s not ideal in a fast-paced project development.

With Figma, engineers see changes in real time, allowing them to participate in every step of the project, from wireframes to design.

Design Programmatically is key for us, so our engineers can simultaneously work on developing components while us, designers, progress with the design creation and copywriters progress with content. We essentially have all of the tools we need to create dynamic, digital products in one place.

## Tabs!

One of my favourite features, and probably something I took for granted in the past is the ability to open projects in tabs.

And damn. It's fast.
And damn. It's fast.
Like a browser, the Figma app allows you to have several tabs open so you can jump back and forth between pages rather than having multiple windows messing up your desktop. I probably increased my efficiency by 50% or more being able to have several projects open, without eating my RAM alive.

## Power to our team

Back to my initial point, collaboration is key for a company like Narative. Especially with a team overseas. Working on Figma, however, regardless of where you are in the world, it’s like working right next to each other.

It’s tough to express just how efficient we’ve become, with everyone having access to one single file, at the same time.
I design simultaneously with our copywriter, while our developer watches our progress, providing relevant comments. Again, it’s magical. Exporting images, SVGs, colors, and even CSS styles, is as simple as right-clicking and copying.

## Conclusion

Figma is not only a full-fledged design tool but the best I’ve used in years. It speaks volumes regarding just how much its creators considered the future.

Witnessing forward-thinking products is not only refreshing but extremely inspirational to know there are teams working hard to support companies such as Narative to succeed. From drafting our first ideas to real prototypes, all while reducing the friction of turning visual concepts into code.

If you're still not sure, you should definitely try it out. It's free.

```js
import React from "react";
import { graphql, useStaticQuery } from "gatsby";
import styled from "@emotion/styled";

import * as SocialIcons from "../../icons/social";
import mediaqueries from "@styles/media";

const icons = {
  dribbble: SocialIcons.DribbbleIcon,
  linkedin: SocialIcons.LinkedinIcon,
  twitter: SocialIcons.TwitterIcon,
  facebook: SocialIcons.FacebookIcon,
  instagram: SocialIcons.InstagramIcon,
  github: SocialIcons.GithubIcon,
};

const socialQuery = graphql`
  {
    allSite {
      edges {
        node {
          siteMetadata {
            social {
              name
              url
            }
          }
        }
      }
    }
  }
`;

function SocialLinks({ fill = "#73737D" }: { fill: string }) {
  const result = useStaticQuery(socialQuery);
  const socialOptions = result.allSite.edges[0].node.siteMetadata.social;

  return (
    <>
      {socialOptions.map(option => {
        const Icon = icons[option.name];

        return (
          <SocialIconContainer
            key={option.name}
            target="_blank"
            rel="noopener"
            data-a11y="false"
            aria-label={`Link to ${option.name}`}
            href={option.url}
          >
            <Icon fill={fill} />
          </SocialIconContainer>
        );
      })}
    </>
  );
}
```

This is another paragraph after the code block.

## This is a secondary heading

```jsx
import React from "react";
import { ThemeProvider } from "theme-ui";
import theme from "./theme";

export default props => <ThemeProvider theme={theme}>{props.children}</ThemeProvider>;
```

At Narative, we’ve been fans of Gatsby from day one, using it to build performant and flexible products for both clients and ourselves. With the growing community interest in Gatsby, we hope to create more resources that make it easier for anyone to grasp the power of this incredible tool.

In this article I’ll explain how Gatsby’s lifecycle works and what the Gatsby specific files are for.

One of the challenges I had when learning Gatsby was trying to understand the Gatsby lifecycle. React introduced me to the concept of a Component Lifecycle, but when I started learning Gatsby I felt at a loss again. I remember looking through example repositories and seeing Gatsby specific files in every project and thinking to myself, “What are these files for? Why are gatsby-node.js, gatsby-browser.js, and gatsby-ssr.js generated in the default starter kit? Can I really delete these files?”

In this article I’ll explain the how Gatsby’s lifecycle works and what the Gatsby specific files are for.

## How does Gatsby work?

To understand what these files are for, we must first understand how Gatsby works. Gatsby is a static site generator that pulls data from sources you provide and generates a website/app for you.

Gatsby requires Node to be installed to run the Bootstrap and Build sequences. Under the hood, Gatsby uses Webpack to build and start a development server amongst other things.

### Step 1

During the Bootstrap sequence, which occurs every time you run $ gatsby develop, there are about 20 events that fire ranging from validating your gatsby-config.js to building the data schemas and pages for your site. For example, the Bootstrap sequence is where Gatsby will create pages. If you want an in depth look of all 20 Bootstrap steps Swyx shared a fantastic Gist that goes into more detail.

### Step 2

The Build sequence is very similar to the Bootstrap sequence, except it’s run with production optimizations and will output static files ready for deployment. Think of it as building your React application in production mode vs development.

### Step 3

And finally, once the generated files are deployed, Gatsby lives in the browser. Gatsby cleverly generates a static website that turns into a web app after initial load, which extends the lifecycle to the browser.

What’s important to remember is that Gatsby’s lifecycle can be aggregated into 3 main sequences:

* Bootstrap
* Build
* Browser
* These three sequences makeup the Gatsby lifecycle.

Parts of the lifecycle are visible when running $ gatsby develop
A peak into the Gatsby lifecycle when running $ gatsby develop
A peak into the Gatsby lifecycle when running $ gatsby develop
If you’re familiar with React and the component lifecycle, Gatsby’s lifecycle is almost the same concept. Just like React’s lifecycle, Gatsby exposes hooks for developers to build on top of. Those lifecycle hooks are accessed through Gatsby specific files such as gatsby-node.js, gatsby-browser.js and gatsby-ssr.js.

What are the Gatsby specific files for?
gatsby-config.js
A place to put all your site configurations such as plugins, metadata, and polyfills. This file is the blueprint of your application and is where Gatsby really shines with its plugin system. When you run $ gatsby develop or $ gatsby build gatsby-config.js is the first file to be read and validated.

Most of your time spent in gatsby-config.js will likely revolve around source plugins, image plugins, offline support, styling options, and site metadata.

gatsby-node.js
Gatsby runs a Node process when you develop or build your website and uses Webpack under the hood to spin up a development server with hot reloading. During the Node process Gatsby will load plugins, check the cache, bootstrap the website, build the data schema, create pages, and deal with some configuration and data management.

Everything that occurs during the Bootstrap and Build sequences occurs in gatsby-node.js. This means it’s the perfect place to create pages dynamically based off data from a source plugin or modify Gatsby’s Webpack or Babel configs.

For example, if you want to move some files manually, such as a Netlify _redirects file, a good place to do it is in your gatsby-node.js file at the onPostBuild lifecycle hook.

From experience, most of my time has revolved around handling data and building pages in gatsby-node.js. This file quickly becomes the piping of your entire website.

## Examples of gatsby-node.js hooks:

* createPages
* onCreateBabelConfig
* onCreateWebpackConfig
* onPostBuild
* gatsby-ssr.js

When you think Server Side Rendering you think of a server that takes in requests and dynamically builds pages and sends it to the client. Gatsby doesn’t do that, but it does server side render — it generates all the pages during build time.

Naturally, gatsby-ssr.js allows developers to hook into that lifecycle. In my experience, most use cases revolve around injecting CSS, HTML, or Redux state information into the generated output. For example, if you need to insert third party scripts such as Analytics Tracking or a Pixel it can be done on the onRenderBody gatsby-ssr.js hook.

## Examples of gatsby-ssr.js hooks:

* onPreRenderHTML
* onRenderBody
* replaceRenderer
* gatsby-browser.js

Gatsby is a static site that loads a dynamic application after initial load, which means you get the benefits of a static site in a web application. gatsby-browser.js provides convenient hooks to deal with app loading, route updates, service worker updates, scroll positioning, and more.

Everything that occurs after your static site has loaded can be hooked in gatsby-browser.js. For apps that I’ve built, gatsby-browser.js was mostly used for keeping track of routes, scroll positioning, and sending analytics events.

## Examples of gatsby-browser.js hooks:

* onClientEntry
* onRouteUpdate
* onServiceWorkerInstalled
* registerServiceWorker
* shouldUpdateScroll

## Conclusion

Gatsby is built with React at its core and shares a common API pattern, the lifecycle. This lifecycle gives developers access to key moments in their website’s process through specific hooks. For example, adding analytics can be achieved through the Browser lifecycle hook onClientEntry. Gatsby reserves specific filenames as an entry point to access every lifecycle; these files are named gatsby-node.js, gatsby-ssr.js and gatsby-browser.js.

Without the Gatsby lifecycle, it would be impossible to customize and modify your project beyond the base configuration, leaving developers with a rigid and poor developer experience. This power and flexibility has helped us build amazing web projects for clients like Hopper!

Gatsby is a staple within our engineering process at Narative, helping us help our clients build the products they’ve always dreamed of, and the ones they’re yet to dream up.