Learning something about OS creation. 
Credit: https://os.phil-opp.com/

# Build for the bare metal target
`cargo build --target thumbv7em-none-eabihf`

# Build for the host system
## Linux
`cargo rustc -- -C link-arg=-nostartfiles`
## Windows
`cargo rustc -- -C link-args="/ENTRY:_start /SUBSYSTEM:console"`
## macOS
`cargo rustc -- -C link-args="-e __start -static -nostartfiles"`