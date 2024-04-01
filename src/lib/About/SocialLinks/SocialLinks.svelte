<script>
    import ghLogo from '$lib/assets/gh-logo.svg';
	import linkedinLogo from '$lib/assets/linkedin-logo.svg';
	import mailLogo from '$lib/assets/mail-logo.svg';
	import leetcodeLogo from '$lib/assets/leetcode-logo.svg';


	const gh = { name: 'github', icon: ghLogo, url: 'https://github.com/vikrantrath' };
	const ln = {
		name: 'linkedin',
		icon: linkedinLogo,
		url: 'https://www.linkedin.com/in/vikrantrath/'
	};
	// const mail = {
	// 	name: 'email',
	// 	icon: mailLogo,
	// 	url: '/contact'
	// };
	const leetcode = {
		name: 'leetcode',
		icon: leetcodeLogo,
		url: 'https://leetcode.com/vikrantrath/'
	};
</script>

<ul class="flex w-1/2 mt-4 gap-5 items-center mb-4">
	<a href={gh.url} target="_blank" rel="noopener noreferrer"
		><img class="w-7" src={gh.icon} alt="github-link" /></a
	>
	<a href={ln.url} target="_blank" rel="noopener noreferrer"
		><img class="w-8" src={ln.icon} alt="linkedin-link" /></a
	>
	<a href={leetcode.url} target="_blank" rel="noopener noreferrer"
		><img class="w-8" src={leetcode.icon} alt="mail-link" /></a
	>
</ul>
