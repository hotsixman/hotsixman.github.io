<script lang="ts">
    import html from '../../assets/skiils/html.svg';
    import css from '../../assets/skiils/css.svg'
    import js from '../../assets/skiils/js.svg';
    import ts from '../../assets/skiils/ts.svg';
    import svelte from '../../assets/skiils/svelte.svg';
    import nodejs from '../../assets/skiils/nodejs.svg';
    import sveltekit from '../../assets/skiils/sveltekit.svg';

    import SkillGroup from "./skill-group.svelte";
    import Skill from "./skill.svelte";
    import TimelineRow from "./timeline-row.svelte";
    import Timeline from "./timeline.svelte";
    import SkillIcon from "./skill-icon.svelte";
</script>

<Timeline>
    <TimelineRow date="2023.4 ~ 2024.2">
        taikowiki.com 개발
    </TimelineRow>
    <TimelineRow date="2023.11 ~">
        node-hiroba 개발
    </TimelineRow>
</Timeline>
<Skill>
    <SkillGroup groupName="Languages">
        <SkillIcon src={html} description="HTML: 웹 페이지를 구성하기 위한 마크업 언어입니다." color="#f16529"/>
        <SkillIcon src={css} description="CSS: HTML이 표시되는 방법을 기술하는 스타일 언어입니다." color="#3c9cd7"/>
        <SkillIcon src={js} description="JavaScript: 동적인 웹페이지를 구성하기 위한 언어입니다." color="#f7df1e"/>
        <SkillIcon src={ts} description="TypeScript: 자바스크립트에 타입 명시 등의 기능이 추가된 언어입니다." color="#007acc"/>
    </SkillGroup>
    <SkillGroup groupName="Frontend Frameworks">
        <SkillIcon src={svelte} description="Svelte: SPA와 컴포넌트 기반 웹페이지 개발을 위한 자바스크립트 프레임워크입니다." color="#ff3e00"/>
    </SkillGroup>
    <SkillGroup groupName="Backend Frameworks">
        <SkillIcon src={nodejs} description="Node.js: 브라우저 밖에서 자바스크립트를 실행할 수 있는 런타임 플랫폼입니다." color="#689f63"/>
    </SkillGroup>
    <SkillGroup groupName="Fullstack Frameworks">
        <SkillIcon src={sveltekit} description="SvelteKit: Svelte 문법을 이용해 웹 서버를 개발할 수 있는 Node.js 프레임워크입니다." color="#ff3e00"/>
    </SkillGroup>
</Skill>