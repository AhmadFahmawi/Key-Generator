# Key-Generator
Simple Key Generator - Generating random 36 alphanumeric characters


# How to use - End users
Download the file, click on Key Generator.html
It will run on your browser, simple hit the Generate a Key button

# For developers
JS script embeded in the html file

        function generateUUID() {
            var d = new Date().getTime();

            if (window.performance && typeof window.performance.now === "function") {
                d += performance.now();
            }

            var uuid = 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function (c) {
                var r = (d + Math.random() * 16) % 16 | 0;
                d = Math.floor(d / 16);
                return (c == 'x' ? r : (r & 0x3 | 0x8)).toString(16);
            });

            return uuid;
        }
