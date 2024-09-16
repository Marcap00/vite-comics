<script>
export default {
    data() {
        return {
            footerLists: [
                {
                    title: 'DC COMICS', 
                    links: [
                    {href: '#', text: 'Characters',},
                    {href: '#', text: 'Comics',},
                    {href: '#', text: 'Movies',},
                    {href: '#', text: 'TV',},
                    {href: '#', text: 'Games',},
                    {href: '#', text: 'Videos',},
                    {href: '#', text: 'News',}
                    ]
                },
                {
                    title: 'DC', 
                    links: [
                    {href: '#', text: 'Term Of Use',},
                    {href: '#', text: 'Privacy Policy (New)',},
                    {href: '#', text: 'Ad Choices',},
                    {href: '#', text: 'Advertising',},
                    {href: '#', text: 'Jobs',},
                    {href: '#', text: 'Subsciptions',},
                    {href: '#', text: 'Talent Workshops',},
                    {href: '#', text: 'CPSC Certification',},
                    {href: '#', text: 'Ratings',},
                    {href: '#', text: 'Shop Help',},
                    {href: '#', text: 'Contact Us',}
                    ]
                },
                {
                    title: 'SITES', 
                    links: [
                    {href: '#', text: 'DC',},
                    {href: '#', text: 'MAD Magazine',},
                    {href: '#', text: 'DC Kids',},
                    {href: '#', text: 'DC Universe',},
                    {href: '#', text: 'DC Power Visa',}
                    ]
                },
                {
                    title: 'SHOP', 
                    links: [
                    {href: '#', text: 'Shop DC',},
                    {href: '#', text: 'Shop DC Collectibles',},
                    
                    ]
                },
            ]

        }
    }
}
</script>

<template>
    
        <ul v-for="(list, index) in footerLists" >
            <li>
                {{ list.title }} 
            </li>
            <li v-for="link in footerLists[index].links">
                <a :href="link.href"> {{ link.text }} </a>
            </li>
        </ul>
    
</template>

<style scoped>

</style>