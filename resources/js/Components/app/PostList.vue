<script setup>
import PostItem from '@/Components/app/PostItem.vue'
const post1= {
    user: {
        id: 1,
        avatar:'https://randomuser.me/api/portraits/men/44.jpg',
        name: 'John Smith'
    },
    attachments: [
        {
            id: 1,
            name: 'test.png',
            url: 'https://picsum.photos/1000',
            mime: 'image/png'
        },
        {
            id: 2,
            name: 'test.png',
            url: 'https://picsum.photos/1000',
            mime: 'image/png'
        },
        {
            id: 3,
            name: 'document.docx',
            url: '#',
            mime: 'apllication/msword'
        }
    ],
    group: null,
    body: `<p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam quaerat nemo dignissimos eius autem tempora laborum eligendi odio fugiat consectetur pariatur laudantium temporibus non dolore, tempore laboriosam iusto ab, sapiente sed aliquid consequuntur itaque quasi quis magni. Quia quo exercitationem aperiam quam facere iste, repudiandae, architecto atque vero tenetur qui!</p>
    <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam quaerat nemo dignissimos eius autem tempora laborum eligendi odio fugiat consectetur pariatur laudantium temporibus non dolore, tempore laboriosam iusto ab, sapiente sed aliquid consequuntur itaque quasi quis magni. Quia quo exercitationem aperiam quam facere iste, repudiandae, architecto atque vero tenetur qui!</p>`,
    created_at: '2024-03-03'

}
const post2= {
    user: {
        id: 2,
        avatar:'https://randomuser.me/api/portraits/men/44.jpg',
        name: 'John Doe'
    },
    group: {
        id: 1,
        name: 'Laravel Developer'
    },
    body: `<p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam quaerat nemo dignissimos eius autem tempora laborum eligendi odio fugiat consectetur pariatur laudantium temporibus non dolore, tempore laboriosam iusto ab, sapiente sed aliquid consequuntur itaque quasi quis magni. Quia quo exercitationem aperiam quam facere iste, repudiandae, architecto atque vero tenetur qui!</p>
    <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam quaerat nemo dignissimos eius autem tempora laborum eligendi odio fugiat consectetur pariatur laudantium temporibus non dolore, tempore laboriosam iusto ab, sapiente sed aliquid consequuntur itaque quasi quis magni. Quia quo exercitationem aperiam quam facere iste, repudiandae, architecto atque vero tenetur qui!</p>`,
    created_at: '2024-03-03'

}
</script>
<template>
    <div class="lg:overflow-scroll h-full lg:h-[500px]">
        <PostItem :post="post1"/>
        <PostItem :post="post2"/>
        <PostItem :post="post1"/>
        <PostItem :post="post2"/>
        <PostItem :post="post1"/>
        <PostItem :post="post2"/>
        <PostItem :post="post1"/>
        <PostItem :post="post2"/>
        <PostItem :post="post1"/>
        <PostItem :post="post2"/>
    </div>
</template>
