# thaibginaframe
Thai translation of Bhagavad Gita to be used as an embed in iframe elements.

Some ISKCON sites want to provide access to Bhagavad Gita but have no facilities to host it themselves or to properly incorporate it in their css and templates. In such cases Bhagavad Gita can be included as an embed, inside the iframe element. Source should be set to https://bgthai.github.io/thaibginaframe 

HTML files in this repository included a javascript that provides height of the rendered iframe to avoid dealing with cross-domain issues. On the host site this can processed by javascript like this:

<script>
    window.addEventListener('message', function(event) {
        // Ensure the message is from a trusted origin
        if (event.origin === 'https://yourhost.com') {
            var iframe = document.getElementById('your-iframe');
            iframe.style.height = event.data + 'px';
        }
    }, false);
</script>

This script should be included on the host site to get heigh information from iframe - this is useful in case you want your page height to adapt to the height of Bhagavad Gita chapters or verses and avoid dealing with two sets of scroll bars etc.

