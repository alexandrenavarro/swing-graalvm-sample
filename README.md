# swing-graalvm-sample
swing-graalvm-sample

# Install graalvm + native-image 
    java sdk install java 21.3.1.r17-grl
    gu install native-image

# Run the agent in target/classes
    java  -agentlib:native-image-agent=config-output-dir=config SwingApp

# Generate native (does not work at the end, eerro in the linker command executed)
    native-image --no-fallback -H:ConfigurationFileDirectories=config -Djava.awt.headless=false --allow-incomplete-classpath  -J-Xmx7G  -Djava.awt.headless=false  SwingApp


