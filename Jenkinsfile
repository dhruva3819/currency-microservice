stage('build') {
    when {
        expression {
            def now = new Date()
            def sdf = new java.text.SimpleDateFormat("MM-dd-yyyy HH:mm")
            sdf.setTimeZone(TimeZone.getTimeZone("Asia/Kolkata")) // your local time zone
            def formatted = sdf.format(now)

            // Block 4 PM to 6 PM on June 26, 2025
            !formatted.matches("06-26-2025 (1[6-7]):\\d{2}")
        }
    }
    steps {
        echo "************ Building the application ************"
    }
}
